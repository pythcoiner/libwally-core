# wally-miniscript-satisfier

> Rewrite libwally-core's miniscript satisfier on top of an AST decoder, ported from rust-miniscript, covering tapscript and segwit v0.

## Overview

The current tapscript miniscript satisfier in `src/psbt.c` (lines 5650–6800) is a hand-rolled byte-cursor pattern matcher. It walks raw Bitcoin Script bytes and dispatches by leading/trailing opcode. This is not the canonical approach used by Bitcoin Core or rust-miniscript, both of which decode script bytes into a typed AST first, then satisfy by AST traversal.

The byte-pattern approach has concrete consequences:
- **Coverage gaps:** `pk_h`, `d:`, `j:`, `n:`, `l:`, `u:`, `t:` wrappers not detected
- **Malleability:** `thresh` greedy reverse-first-k selection produces witnesses that a third party could swap (rust-miniscript's `(sat_weight − dissat_weight)` sort + `has_sig` tiebreaker rejects those)
- **32-byte push ambiguity** in `scan_miniscript_expr`: any 32-byte push treated as candidate `pk_k` start
- **Hardcoded `MULTI_A_MAX_KEYS = 20`** truncates silently versus BIP-342's 999 limit

This project replaces the byte-pattern code with a decode→AST→satisfy pipeline that mirrors **rust-miniscript** at a pinned commit, eliminating these issues categorically. It also splits oversized existing commits in the branch (e.g., `b56da26c ("musig2: add MuSig2 (BIP-327) C API") +2176 LoC`, `acf1d67b ("tests: add MuSig2, descriptor and BIP-327/328/373/390 test suites") +4902 LoC`) into reviewer-friendly chunks via interactive rebase.

## Reference

**Primary:** rust-miniscript pinned at `1834bc0635278b0fcdb6b6b2ebe3a7fef2b8154e`
- `src/miniscript/lex.rs` — tokenizer
- `src/miniscript/decode.rs:90–162` (Terminal), `:303–342` (TerminalStack), `:349–425` (parse_insane)
- `src/miniscript/satisfy/mod.rs` — `Witness<T>`, `Satisfaction<T>`, fragment satisfiers
- `src/miniscript/satisfy/sat_dissat.rs` — `(sat, dissat)` per fragment

**Cross-references:** Bitcoin Core `src/script/miniscript.{h,cpp}`, BIP-379

## Goals

- Replace byte-pattern satisfier with AST-based pipeline
- Eliminate malleability bugs and fragment coverage gaps
- Wire `finalize_p2wsh` (currently a stub) to actually finalize segwit v0 miniscript
- Improve commit history granularity (split oversized existing commits)
- Reuse existing `ms_node` AST type from `src/descriptor.c`

## Success Criteria

- [ ] Decoder produces correct AST for all BIP-379 fragments (tapscript + segwit v0), verified by round-trip vs descriptor parser output
- [ ] Rewritten satisfier produces non-malleable witnesses matching rust-miniscript byte-for-byte on a fixed corpus
- [ ] `finalize_p2wsh` produces valid witnesses for all supported fragments
- [ ] All existing taproot tests continue to pass
- [ ] Every commit in the rebased history builds cleanly (bisectability)

## Architecture

### Components

1. **Tokenizer** (`src/miniscript_decode.c`) — Bitcoin Script bytes → token stream. Mirrors rust-miniscript `lex.rs`. Handles 32-byte push disambiguation (KEY32 vs HASH32 vs raw data via look-ahead).

2. **Decoder** (`src/miniscript_decode.c`) — token stream → `ms_node` AST. Iterative state machine using `nonterm` and `terminal` stacks. Mirrors rust-miniscript `decode.rs::parse_insane`.

3. **Satisfaction primitives** (`src/miniscript_satisfy.c`) — `struct ms_satisfaction { has_sig, weight, witness, missing_sigs[], missing_preimages[] }`. Branch selection helpers (`best`, `or_*`, `andor`, `thresh` with malleability check). Mirrors rust-miniscript `satisfy/mod.rs`.

4. **AST satisfier** (`src/miniscript_satisfy.c`) — `satisfy_node(input, node, leaf_hash, ctx_flags, sat, dsat)`. Recursive walk computing both satisfaction and dissatisfaction per fragment. Replaces all byte-pattern code in `src/psbt.c`.

5. **Finalization wiring** (`src/psbt.c`) — `finalize_p2wsh` and `finalize_p2tr_script_path` call `satisfy_node` with the appropriate context flag. Existing entry points `finalize_multisig`, `finalize_csv2of2_1` keep their signatures but bodies call into the generic satisfier.

### Data Flow

```
PSBT input
  → decoded leaf script bytes (PSBT_IN_TAP_LEAF_SCRIPT or PSBT_IN_WITNESS_SCRIPT)
  → tokenize_script(bytes) → token stream
  → decode_script_to_node(tokens) → ms_node AST
  → satisfy_node(input, ast, ctx_flags) → ms_satisfaction
  → wally_psbt_input.final_witness
```

## Phases

This work integrates into the existing branch via interactive rebase starting at `c5fbd2ef ("script: add WALLY_LEAF_VERSION_TAPSCRIPT constant")`. Phases are grouped into 11 cm phases that together produce ~94 commits (vs the 14 we have now).

### Phase 1: Share AST types (1 task)

Move `ms_node` + `g_builtins[]` from `src/descriptor.c` to `src/descriptor_int.h` so the new decoder can reuse them.

### Phase 2: Split existing taproot commits (3 tasks)

Split `de8d0d8f` ("descriptor: add tr() parser, taptree, and BIP-341 tweak"), `5e1ec21a ("descriptor: add taproot leaf and key accessor APIs")`, `635f74df ("psbt: add taproot script-path field support and signing")` into reviewer-friendly chunks (each existing commit currently >500 LoC).

### Phase 3: Tokenizer (5 tasks)

Token enum, opcode-only tokenizer, data tokens with disambiguation, NUM token, unit tests.

### Phase 4: Decoder (11 tasks)

Iterative state machine, then per-fragment-family decode arms.

### Phase 5: Satisfaction primitives (5 tasks)

`ms_satisfaction` struct, selection helpers (`best`, `or_*`, `andor`, `thresh`).

### Phase 6: AST satisfier (11 tasks)

Outer dispatch + per-fragment satisfaction logic.

### Phase 7: Finalization wiring (4 tasks)

`finalize_p2wsh`, `finalize_p2tr_script_path`, remap `finalize_multisig` and `finalize_csv2of2_1`.

### Phase 8: Keep taproot test commits (2 tasks)

Keep existing test commits; AMEND only if witness shape changes break a fixture.

### Phase 9: Split MuSig2 commits (6 tasks)

Split `b56da26c ("musig2: add MuSig2 (BIP-327) C API")`, `5ace65aa ("descriptor: support musig() key expressions (BIP-390)")`, `6346d02d ("psbt: add BIP-373 MuSig2 fields, signing and finalization")`, `acf1d67b ("tests: add MuSig2, descriptor and BIP-327/328/373/390 test suites")`, `41a408ae ("docs: document MuSig2 API and add 2-of-2 PSBT example")` (oversized MuSig2 commits) into per-BIP-step parts.

### Phase 10: New satisfier tests (16 tasks)

Per-fragment round-trip + dissat tests, BIP-379 vectors imported from rust-miniscript, differential test harness.

### Phase 11: Amend tip (1 task)

Update `TODO.md` to reflect what's done.

## Out of Scope

- Elements/Liquid taproot support (separately tracked)
- New public API surface beyond what's needed for finalization
- Bitcoin Core port (rust-miniscript chosen as primary reference)
- Performance optimization beyond what falls out of the algorithm

## References

- [rust-miniscript](https://github.com/rust-bitcoin/rust-miniscript) (pinned at `1834bc0635278b0fcdb6b6b2ebe3a7fef2b8154e`)
- [Bitcoin Core miniscript](https://github.com/bitcoin/bitcoin/blob/master/src/script/miniscript.cpp)
- [BIP-379: Miniscript](https://github.com/bitcoin/bips/blob/master/bip-0379.md)
- [BIP-342: Tapscript](https://github.com/bitcoin/bips/blob/master/bip-0342.mediawiki)
- [BIP-371: Taproot PSBT fields](https://github.com/bitcoin/bips/blob/master/bip-0371.mediawiki)
- Detailed plan: `/home/pyth/.claude/plans/fluffy-dazzling-robin.md`
