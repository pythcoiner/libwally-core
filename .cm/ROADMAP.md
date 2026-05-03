# wally-miniscript-satisfier - Roadmap

This document tracks implementation progress. Check off items as they are completed.

## Phase 1: Move ms_node + g_builtins to descriptor_int.h

Status: **Complete** (1/1)

- [x] Move ms_node + g_builtins to descriptor_int.h

---

## Phase 2: Split de8d0d8f "descriptor: add tr() parser, taptree, and BIP-341 tweak" into 3 parts

Status: **Complete** (1/1)

- [x] Split de8d0d8f "descriptor: add tr() parser, taptree, and BIP-341 tweak" into 3 parts

---

## Phase 3: Split 5e1ec21a "descriptor: add taproot leaf and key accessor APIs" into 3 parts

Status: **Complete** (1/1)

- [x] Split 5e1ec21a "descriptor: add taproot leaf and key accessor APIs" into 3 parts

---

## Phase 4: Split 635f74df "psbt: add taproot script-path field support and signing" into 3 parts

Status: **Complete** (1/1)

- [x] Split 635f74df "psbt: add taproot script-path field support and signing" into 3 parts

---

## Phase 5: tk_kind enum + struct token + miniscript_decode.h skeleton

Status: **Complete** (1/1)

- [x] tk_kind enum + struct token + miniscript_decode.h skeleton

---

## Phase 6: tokenize_script opcode-only path

Status: **Complete** (1/1)

- [x] tokenize_script opcode-only path

---

## Phase 7: Data tokens KEY32/KEY33/HASH20/HASH32 + 32-byte disambiguation

Status: **Complete** (1/1)

- [x] Data tokens KEY32/KEY33/HASH20/HASH32 + 32-byte disambiguation

---

## Phase 8: NUM token parsing (script numbers)

Status: **Complete** (1/1)

- [x] NUM token parsing (script numbers)

---

## Phase 9: Tokenizer unit tests

Status: **Complete** (1/1)

- [x] Tokenizer unit tests

---

## Phase 10: NonTerm enum + terminal_stack helpers

Status: **Complete** (1/1)

- [x] NonTerm enum + terminal_stack helpers

---

## Phase 11: decode_script_to_node outer loop

Status: **Complete** (1/1)

- [x] decode_script_to_node outer loop

---

## Phase 12: Decoder: pk_k / pk_h

Status: **Complete** (1/1)

- [x] Decoder: pk_k / pk_h

---

## Phase 13: Decoder: hash fragments

Status: **Complete** (1/1)

- [x] Decoder: hash fragments

---

## Phase 14: Decoder: timelocks

Status: **Complete** (1/1)

- [x] Decoder: timelocks

---

## Phase 15: Decoder: multi (segwit v0)

Status: **Complete** (1/1)

- [x] Decoder: multi (segwit v0)

---

## Phase 16: Decoder: multi_a (999 limit from start)

Status: **Complete** (1/1)

- [x] Decoder: multi_a (999 limit from start)

---

## Phase 17: Decoder: and_v / and_b

Status: **Complete** (1/1)

- [x] Decoder: and_v / and_b

---

## Phase 18: Decoder: or_* + andor

Status: **Complete** (1/1)

- [x] Decoder: or_* + andor

---

## Phase 19: Decoder: thresh

Status: **Complete** (1/1)

- [x] Decoder: thresh

---

## Phase 20: Decoder: wrappers (a:s:c:d:v:j:n:l:u:t:)

Status: **Complete** (1/1)

- [x] Decoder: wrappers (a:s:c:d:v:j:n:l:u:t:)

---

## Phase 21: ms_witness + ms_satisfaction structs (with failure-reporting fields)

Status: **Complete** (1/1)

- [x] ms_witness + ms_satisfaction structs (with failure-reporting fields)

---

## Phase 22: satisfaction_best

Status: **Complete** (1/1)

- [x] satisfaction_best

---

## Phase 23: satisfaction_or_* selectors

Status: **Complete** (1/1)

- [x] satisfaction_or_* selectors

---

## Phase 24: satisfaction_andor

Status: **Complete** (1/1)

- [x] satisfaction_andor

---

## Phase 25: satisfaction_thresh (DP + malleability check)

Status: **Complete** (1/1)

- [x] satisfaction_thresh (DP + malleability check)

---

## Phase 26: satisfy_node outer dispatch + initial docs/source/satisfier.rst

Status: **Complete** (1/1)

- [x] satisfy_node outer dispatch + initial docs/source/satisfier.rst

---

## Phase 27: Satisfy: pk_k / pk_h

Status: **Complete** (1/1)

- [x] Satisfy: pk_k / pk_h

---

## Phase 28: Satisfy: hash fragments

Status: **Complete** (1/1)

- [x] Satisfy: hash fragments

---

## Phase 29: Satisfy: timelocks

Status: **Complete** (1/1)

- [x] Satisfy: timelocks

---

## Phase 30: Satisfy: multi

Status: **Complete** (1/1)

- [x] Satisfy: multi

---

## Phase 31: Satisfy: multi_a

Status: **Complete** (1/1)

- [x] Satisfy: multi_a

---

## Phase 32: Satisfy: and_v / and_b

Status: **Complete** (1/1)

- [x] Satisfy: and_v / and_b

---

## Phase 33: Satisfy: or_*

Status: **Complete** (1/1)

- [x] Satisfy: or_*

---

## Phase 34: Satisfy: andor

Status: **Complete** (1/1)

- [x] Satisfy: andor

---

## Phase 35: Satisfy: thresh

Status: **Complete** (1/1)

- [x] Satisfy: thresh

---

## Phase 36: Satisfy: wrappers

Status: **Complete** (1/1)

- [x] Satisfy: wrappers

---

## Phase 37: finalize_p2wsh calling new satisfier

Status: **Complete** (1/1)

- [x] finalize_p2wsh calling new satisfier

---

## Phase 38: finalize_p2tr_script_path on new satisfier

Status: **Complete** (1/1)

- [x] finalize_p2tr_script_path on new satisfier

---

## Phase 39: Remap finalize_multisig body

Status: **Complete** (1/1)

- [x] Remap finalize_multisig body

---

## Phase 40: Remap finalize_csv2of2_1 body

Status: **Complete** (1/1)

- [x] Remap finalize_csv2of2_1 body

---

## Phase 41: Keep a50ced46 "tests: add taproot descriptor parsing and address vectors" tests: taproot descriptor parsing

Status: **Complete** (1/1)

- [x] Keep a50ced46 "tests: add taproot descriptor parsing and address vectors" tests: taproot descriptor parsing

---

## Phase 42: Keep/Amend bbd832ad "tests: add taproot miniscript and PSBT script-path test functions" tests: taproot miniscript

Status: **Complete** (1/1)

- [x] Keep/Amend bbd832ad "tests: add taproot miniscript and PSBT script-path test functions" tests: taproot miniscript

---

## Phase 43: Split b56da26c "musig2: add MuSig2 (BIP-327) C API" (MuSig2 BIP-327 API) into 6 parts

Status: **In Progress** (0/1)

- [ ] Split b56da26c "musig2: add MuSig2 (BIP-327) C API" (MuSig2 BIP-327 API) into 6 parts

---

## Phase 44: Split 5ace65aa "descriptor: support musig() key expressions (BIP-390)" (musig() descriptor BIP-390) into 3 parts

Status: **Not Started** (0/1)

- [ ] Split 5ace65aa "descriptor: support musig() key expressions (BIP-390)" (musig() descriptor BIP-390) into 3 parts

---

## Phase 45: Split 6346d02d "psbt: add BIP-373 MuSig2 fields, signing and finalization" (PSBT BIP-373 MuSig2) into 6 parts

Status: **Not Started** (0/1)

- [ ] Split 6346d02d "psbt: add BIP-373 MuSig2 fields, signing and finalization" (PSBT BIP-373 MuSig2) into 6 parts

---

## Phase 46: Keep aafbc5bc "fuzz: add fuzzers for musig() descriptor and PSBT MuSig2 fields" fuzz commit

Status: **Not Started** (0/1)

- [ ] Keep aafbc5bc "fuzz: add fuzzers for musig() descriptor and PSBT MuSig2 fields" fuzz commit

---

## Phase 47: Split acf1d67b "tests: add MuSig2, descriptor and BIP-327/328/373/390 test suites" (MuSig2 test suites) into 5 parts

Status: **Not Started** (0/1)

- [ ] Split acf1d67b "tests: add MuSig2, descriptor and BIP-327/328/373/390 test suites" (MuSig2 test suites) into 5 parts

---

## Phase 48: Split 41a408ae "docs: document MuSig2 API and add 2-of-2 PSBT example" (MuSig2 docs) into 2 parts

Status: **Not Started** (0/1)

- [ ] Split 41a408ae "docs: document MuSig2 API and add 2-of-2 PSBT example" (MuSig2 docs) into 2 parts

---

## Phase 49: Test: pk_k / pk_h

Status: **Not Started** (0/1)

- [ ] Test: pk_k / pk_h

---

## Phase 50: Test: hash fragments

Status: **Not Started** (0/1)

- [ ] Test: hash fragments

---

## Phase 51: Test: timelocks

Status: **Not Started** (0/1)

- [ ] Test: timelocks

---

## Phase 52: Test: multi

Status: **Not Started** (0/1)

- [ ] Test: multi

---

## Phase 53: Test: multi_a

Status: **Not Started** (0/1)

- [ ] Test: multi_a

---

## Phase 54: Test: and_v / and_b

Status: **Not Started** (0/1)

- [ ] Test: and_v / and_b

---

## Phase 55: Test: or_*

Status: **Not Started** (0/1)

- [ ] Test: or_*

---

## Phase 56: Test: andor

Status: **Not Started** (0/1)

- [ ] Test: andor

---

## Phase 57: Test: thresh

Status: **Not Started** (0/1)

- [ ] Test: thresh

---

## Phase 58: Test: wrappers

Status: **Not Started** (0/1)

- [ ] Test: wrappers

---

## Phase 59: Test: composite descriptors (Liana template, etc.)

Status: **Not Started** (0/1)

- [ ] Test: composite descriptors (Liana template, etc.)

---

## Phase 60: Test: negative cases

Status: **Not Started** (0/1)

- [ ] Test: negative cases

---

## Phase 61: Test: BIP-379 vectors imported from rust-miniscript

Status: **Not Started** (0/1)

- [ ] Test: BIP-379 vectors imported from rust-miniscript

---

## Phase 62: Test: differential test harness scaffolding

Status: **Not Started** (0/1)

- [ ] Test: differential test harness scaffolding

---

## Phase 63: Test: differential corpus runner

Status: **Not Started** (0/1)

- [ ] Test: differential corpus runner

---

## Phase 64: Test: regression smoke (existing taproot witnesses identical)

Status: **Not Started** (0/1)

- [ ] Test: regression smoke (existing taproot witnesses identical)

---

## Phase 65: Update TODO.md to reflect what's done

Status: **Not Started** (0/1)

- [ ] Update TODO.md to reflect what's done

---
