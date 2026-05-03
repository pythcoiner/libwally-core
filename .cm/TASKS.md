# wally-miniscript-satisfier - Tasks

This document shows phase plans and task status. Generated from tasks.json.

## phase-1: Move ms_node + g_builtins to descriptor_int.h

**Status:** Complete (1/1)

### Tasks

- [x] **phase-1.task-1**: Move ms_node + g_builtins to descriptor_int.h

---

## phase-2: Split de8d0d8f "descriptor: add tr() parser, taptree, and BIP-341 tweak" into 3 parts

**Status:** Complete (1/1)

### Tasks

- [x] **phase-2.task-1**: Split de8d0d8f "descriptor: add tr() parser, taptree, and BIP-341 tweak" into 3 parts

---

## phase-3: Split 5e1ec21a "descriptor: add taproot leaf and key accessor APIs" into 3 parts

**Status:** Complete (1/1)

### Tasks

- [x] **phase-3.task-1**: Split 5e1ec21a "descriptor: add taproot leaf and key accessor APIs" into 3 parts

---

## phase-4: Split 635f74df "psbt: add taproot script-path field support and signing" into 3 parts

**Status:** Complete (1/1)

### Tasks

- [x] **phase-4.task-1**: Split 635f74df "psbt: add taproot script-path field support and signing" into 3 parts

---

## phase-5: tk_kind enum + struct token + miniscript_decode.h skeleton

**Status:** Complete (1/1)

### Tasks

- [x] **phase-5.task-1**: tk_kind enum + struct token + miniscript_decode.h skeleton

---

## phase-6: tokenize_script opcode-only path

**Status:** Complete (1/1)

### Tasks

- [x] **phase-6.task-1**: tokenize_script opcode-only path

---

## phase-7: Data tokens KEY32/KEY33/HASH20/HASH32 + 32-byte disambiguation

**Status:** Complete (1/1)

### Tasks

- [x] **phase-7.task-1**: Data tokens KEY32/KEY33/HASH20/HASH32 + 32-byte disambiguation

---

## phase-8: NUM token parsing (script numbers)

**Status:** Complete (1/1)

### Tasks

- [x] **phase-8.task-1**: NUM token parsing (script numbers)

---

## phase-9: Tokenizer unit tests

**Status:** Complete (1/1)

### Tasks

- [x] **phase-9.task-1**: Tokenizer unit tests

---

## phase-10: NonTerm enum + terminal_stack helpers

**Status:** Complete (1/1)

### Tasks

- [x] **phase-10.task-1**: NonTerm enum + terminal_stack helpers

---

## phase-11: decode_script_to_node outer loop

**Status:** Complete (1/1)

### Tasks

- [x] **phase-11.task-1**: decode_script_to_node outer loop

---

## phase-12: Decoder: pk_k / pk_h

**Status:** Complete (1/1)

### Tasks

- [x] **phase-12.task-1**: Decoder: pk_k / pk_h

---

## phase-13: Decoder: hash fragments

**Status:** Complete (1/1)

### Tasks

- [x] **phase-13.task-1**: Decoder: hash fragments

---

## phase-14: Decoder: timelocks

**Status:** Complete (1/1)

### Tasks

- [x] **phase-14.task-1**: Decoder: timelocks

---

## phase-15: Decoder: multi (segwit v0)

**Status:** Complete (1/1)

### Tasks

- [x] **phase-15.task-1**: Decoder: multi (segwit v0)

---

## phase-16: Decoder: multi_a (999 limit from start)

**Status:** Complete (1/1)

### Tasks

- [x] **phase-16.task-1**: Decoder: multi_a (999 limit from start)

---

## phase-17: Decoder: and_v / and_b

**Status:** Complete (1/1)

### Tasks

- [x] **phase-17.task-1**: Decoder: and_v / and_b

---

## phase-18: Decoder: or_* + andor

**Status:** Complete (1/1)

### Tasks

- [x] **phase-18.task-1**: Decoder: or_* + andor

---

## phase-19: Decoder: thresh

**Status:** Complete (1/1)

### Tasks

- [x] **phase-19.task-1**: Decoder: thresh

---

## phase-20: Decoder: wrappers (a:s:c:d:v:j:n:l:u:t:)

**Status:** Complete (1/1)

### Tasks

- [x] **phase-20.task-1**: Decoder: wrappers (a:s:c:d:v:j:n:l:u:t:)

---

## phase-21: ms_witness + ms_satisfaction structs (with failure-reporting fields)

**Status:** Complete (1/1)

### Tasks

- [x] **phase-21.task-1**: ms_witness + ms_satisfaction structs (with failure-reporting fields)

---

## phase-22: satisfaction_best

**Status:** Complete (1/1)

### Tasks

- [x] **phase-22.task-1**: satisfaction_best

---

## phase-23: satisfaction_or_* selectors

**Status:** Complete (1/1)

### Tasks

- [x] **phase-23.task-1**: satisfaction_or_* selectors

---

## phase-24: satisfaction_andor

**Status:** Complete (1/1)

### Tasks

- [x] **phase-24.task-1**: satisfaction_andor

---

## phase-25: satisfaction_thresh (DP + malleability check)

**Status:** Complete (1/1)

### Tasks

- [x] **phase-25.task-1**: satisfaction_thresh (DP + malleability check)

---

## phase-26: satisfy_node outer dispatch + initial docs/source/satisfier.rst

**Status:** Complete (1/1)

### Tasks

- [x] **phase-26.task-1**: satisfy_node outer dispatch + initial docs/source/satisfier.rst

---

## phase-27: Satisfy: pk_k / pk_h

**Status:** Complete (1/1)

### Tasks

- [x] **phase-27.task-1**: Satisfy: pk_k / pk_h

---

## phase-28: Satisfy: hash fragments

**Status:** Complete (1/1)

### Tasks

- [x] **phase-28.task-1**: Satisfy: hash fragments

---

## phase-29: Satisfy: timelocks

**Status:** Complete (1/1)

### Tasks

- [x] **phase-29.task-1**: Satisfy: timelocks

---

## phase-30: Satisfy: multi

**Status:** Complete (1/1)

### Tasks

- [x] **phase-30.task-1**: Satisfy: multi

---

## phase-31: Satisfy: multi_a

**Status:** Complete (1/1)

### Tasks

- [x] **phase-31.task-1**: Satisfy: multi_a

---

## phase-32: Satisfy: and_v / and_b

**Status:** Complete (1/1)

### Tasks

- [x] **phase-32.task-1**: Satisfy: and_v / and_b

---

## phase-33: Satisfy: or_*

**Status:** Complete (1/1)

### Tasks

- [x] **phase-33.task-1**: Satisfy: or_*

---

## phase-34: Satisfy: andor

**Status:** Complete (1/1)

### Tasks

- [x] **phase-34.task-1**: Satisfy: andor

---

## phase-35: Satisfy: thresh

**Status:** Complete (1/1)

### Tasks

- [x] **phase-35.task-1**: Satisfy: thresh

---

## phase-36: Satisfy: wrappers

**Status:** Complete (1/1)

### Tasks

- [x] **phase-36.task-1**: Satisfy: wrappers

---

## phase-37: finalize_p2wsh calling new satisfier

**Status:** Complete (1/1)

### Tasks

- [x] **phase-37.task-1**: finalize_p2wsh calling new satisfier

---

## phase-38: finalize_p2tr_script_path on new satisfier

**Status:** Complete (1/1)

### Tasks

- [x] **phase-38.task-1**: finalize_p2tr_script_path on new satisfier

---

## phase-39: Remap finalize_multisig body

**Status:** Complete (1/1)

### Tasks

- [x] **phase-39.task-1**: Remap finalize_multisig body

---

## phase-40: Remap finalize_csv2of2_1 body

**Status:** Complete (1/1)

### Tasks

- [x] **phase-40.task-1**: Remap finalize_csv2of2_1 body

---

## phase-41: Keep a50ced46 "tests: add taproot descriptor parsing and address vectors" tests: taproot descriptor parsing

**Status:** Complete (1/1)

### Tasks

- [x] **phase-41.task-1**: Keep a50ced46 "tests: add taproot descriptor parsing and address vectors" tests: taproot descriptor parsing

---

## phase-42: Keep/Amend bbd832ad "tests: add taproot miniscript and PSBT script-path test functions" tests: taproot miniscript

**Status:** Complete (1/1)

### Tasks

- [x] **phase-42.task-1**: Keep/Amend bbd832ad "tests: add taproot miniscript and PSBT script-path test functions" tests: taproot miniscript

---

## phase-43: Split b56da26c "musig2: add MuSig2 (BIP-327) C API" (MuSig2 BIP-327 API) into 6 parts

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-43.task-1**: Split b56da26c "musig2: add MuSig2 (BIP-327) C API" (MuSig2 BIP-327 API) into 6 parts

---

## phase-44: Split 5ace65aa "descriptor: support musig() key expressions (BIP-390)" (musig() descriptor BIP-390) into 3 parts

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-44.task-1**: Split 5ace65aa "descriptor: support musig() key expressions (BIP-390)" (musig() descriptor BIP-390) into 3 parts

---

## phase-45: Split 6346d02d "psbt: add BIP-373 MuSig2 fields, signing and finalization" (PSBT BIP-373 MuSig2) into 6 parts

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-45.task-1**: Split 6346d02d "psbt: add BIP-373 MuSig2 fields, signing and finalization" (PSBT BIP-373 MuSig2) into 6 parts

---

## phase-46: Keep aafbc5bc "fuzz: add fuzzers for musig() descriptor and PSBT MuSig2 fields" fuzz commit

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-46.task-1**: Keep aafbc5bc "fuzz: add fuzzers for musig() descriptor and PSBT MuSig2 fields" fuzz commit

---

## phase-47: Split acf1d67b "tests: add MuSig2, descriptor and BIP-327/328/373/390 test suites" (MuSig2 test suites) into 5 parts

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-47.task-1**: Split acf1d67b "tests: add MuSig2, descriptor and BIP-327/328/373/390 test suites" (MuSig2 test suites) into 5 parts

---

## phase-48: Split 41a408ae "docs: document MuSig2 API and add 2-of-2 PSBT example" (MuSig2 docs) into 2 parts

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-48.task-1**: Split 41a408ae "docs: document MuSig2 API and add 2-of-2 PSBT example" (MuSig2 docs) into 2 parts

---

## phase-49: Test: pk_k / pk_h

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-49.task-1**: Test: pk_k / pk_h

---

## phase-50: Test: hash fragments

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-50.task-1**: Test: hash fragments

---

## phase-51: Test: timelocks

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-51.task-1**: Test: timelocks

---

## phase-52: Test: multi

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-52.task-1**: Test: multi

---

## phase-53: Test: multi_a

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-53.task-1**: Test: multi_a

---

## phase-54: Test: and_v / and_b

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-54.task-1**: Test: and_v / and_b

---

## phase-55: Test: or_*

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-55.task-1**: Test: or_*

---

## phase-56: Test: andor

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-56.task-1**: Test: andor

---

## phase-57: Test: thresh

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-57.task-1**: Test: thresh

---

## phase-58: Test: wrappers

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-58.task-1**: Test: wrappers

---

## phase-59: Test: composite descriptors (Liana template, etc.)

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-59.task-1**: Test: composite descriptors (Liana template, etc.)

---

## phase-60: Test: negative cases

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-60.task-1**: Test: negative cases

---

## phase-61: Test: BIP-379 vectors imported from rust-miniscript

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-61.task-1**: Test: BIP-379 vectors imported from rust-miniscript

---

## phase-62: Test: differential test harness scaffolding

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-62.task-1**: Test: differential test harness scaffolding

---

## phase-63: Test: differential corpus runner

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-63.task-1**: Test: differential corpus runner

---

## phase-64: Test: regression smoke (existing taproot witnesses identical)

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-64.task-1**: Test: regression smoke (existing taproot witnesses identical)

---

## phase-65: Update TODO.md to reflect what's done

**Status:** Pending (0/1)

### Tasks

- [ ] **phase-65.task-1**: Update TODO.md to reflect what's done

---

## Summary

**Total progress: 42/65 tasks completed**

| Phase | Status | Total | Done |
|-------|--------|-------|------|
| phase-1: Move ms_node + g_builtins to descriptor_... | Complete | 1 | 1 |
| phase-2: Split de8d0d8f "descriptor: add tr() par... | Complete | 1 | 1 |
| phase-3: Split 5e1ec21a "descriptor: add taproot ... | Complete | 1 | 1 |
| phase-4: Split 635f74df "psbt: add taproot script... | Complete | 1 | 1 |
| phase-5: tk_kind enum + struct token + miniscript... | Complete | 1 | 1 |
| phase-6: tokenize_script opcode-only path | Complete | 1 | 1 |
| phase-7: Data tokens KEY32/KEY33/HASH20/HASH32 + ... | Complete | 1 | 1 |
| phase-8: NUM token parsing (script numbers) | Complete | 1 | 1 |
| phase-9: Tokenizer unit tests | Complete | 1 | 1 |
| phase-10: NonTerm enum + terminal_stack helpers | Complete | 1 | 1 |
| phase-11: decode_script_to_node outer loop | Complete | 1 | 1 |
| phase-12: Decoder: pk_k / pk_h | Complete | 1 | 1 |
| phase-13: Decoder: hash fragments | Complete | 1 | 1 |
| phase-14: Decoder: timelocks | Complete | 1 | 1 |
| phase-15: Decoder: multi (segwit v0) | Complete | 1 | 1 |
| phase-16: Decoder: multi_a (999 limit from start) | Complete | 1 | 1 |
| phase-17: Decoder: and_v / and_b | Complete | 1 | 1 |
| phase-18: Decoder: or_* + andor | Complete | 1 | 1 |
| phase-19: Decoder: thresh | Complete | 1 | 1 |
| phase-20: Decoder: wrappers (a:s:c:d:v:j:n:l:u:t:) | Complete | 1 | 1 |
| phase-21: ms_witness + ms_satisfaction structs (wi... | Complete | 1 | 1 |
| phase-22: satisfaction_best | Complete | 1 | 1 |
| phase-23: satisfaction_or_* selectors | Complete | 1 | 1 |
| phase-24: satisfaction_andor | Complete | 1 | 1 |
| phase-25: satisfaction_thresh (DP + malleability c... | Complete | 1 | 1 |
| phase-26: satisfy_node outer dispatch + initial do... | Complete | 1 | 1 |
| phase-27: Satisfy: pk_k / pk_h | Complete | 1 | 1 |
| phase-28: Satisfy: hash fragments | Complete | 1 | 1 |
| phase-29: Satisfy: timelocks | Complete | 1 | 1 |
| phase-30: Satisfy: multi | Complete | 1 | 1 |
| phase-31: Satisfy: multi_a | Complete | 1 | 1 |
| phase-32: Satisfy: and_v / and_b | Complete | 1 | 1 |
| phase-33: Satisfy: or_* | Complete | 1 | 1 |
| phase-34: Satisfy: andor | Complete | 1 | 1 |
| phase-35: Satisfy: thresh | Complete | 1 | 1 |
| phase-36: Satisfy: wrappers | Complete | 1 | 1 |
| phase-37: finalize_p2wsh calling new satisfier | Complete | 1 | 1 |
| phase-38: finalize_p2tr_script_path on new satisfi... | Complete | 1 | 1 |
| phase-39: Remap finalize_multisig body | Complete | 1 | 1 |
| phase-40: Remap finalize_csv2of2_1 body | Complete | 1 | 1 |
| phase-41: Keep a50ced46 "tests: add taproot descri... | Complete | 1 | 1 |
| phase-42: Keep/Amend bbd832ad "tests: add taproot ... | Complete | 1 | 1 |
| phase-43: Split b56da26c "musig2: add MuSig2 (BIP-... | Pending | 1 | 0 |
| phase-44: Split 5ace65aa "descriptor: support musi... | Pending | 1 | 0 |
| phase-45: Split 6346d02d "psbt: add BIP-373 MuSig2... | Pending | 1 | 0 |
| phase-46: Keep aafbc5bc "fuzz: add fuzzers for mus... | Pending | 1 | 0 |
| phase-47: Split acf1d67b "tests: add MuSig2, descr... | Pending | 1 | 0 |
| phase-48: Split 41a408ae "docs: document MuSig2 AP... | Pending | 1 | 0 |
| phase-49: Test: pk_k / pk_h | Pending | 1 | 0 |
| phase-50: Test: hash fragments | Pending | 1 | 0 |
| phase-51: Test: timelocks | Pending | 1 | 0 |
| phase-52: Test: multi | Pending | 1 | 0 |
| phase-53: Test: multi_a | Pending | 1 | 0 |
| phase-54: Test: and_v / and_b | Pending | 1 | 0 |
| phase-55: Test: or_* | Pending | 1 | 0 |
| phase-56: Test: andor | Pending | 1 | 0 |
| phase-57: Test: thresh | Pending | 1 | 0 |
| phase-58: Test: wrappers | Pending | 1 | 0 |
| phase-59: Test: composite descriptors (Liana templ... | Pending | 1 | 0 |
| phase-60: Test: negative cases | Pending | 1 | 0 |
| phase-61: Test: BIP-379 vectors imported from rust... | Pending | 1 | 0 |
| phase-62: Test: differential test harness scaffold... | Pending | 1 | 0 |
| phase-63: Test: differential corpus runner | Pending | 1 | 0 |
| phase-64: Test: regression smoke (existing taproot... | Pending | 1 | 0 |
| phase-65: Update TODO.md to reflect what's done | Pending | 1 | 0 |