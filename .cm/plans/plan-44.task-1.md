# phase-44.task-1: Split 5ace65aa "descriptor: support musig() key expressions (BIP-390)" (musig() descriptor BIP-390) into 3 parts

## Goal

Split 5ace65aa "descriptor: support musig() key expressions (BIP-390)" (musig() descriptor BIP-390) into 3 parts

## Type
implement

## Status
pending

## Files to read
- `src/descriptor.c`

## Reference
Primary: rust-miniscript pinned at `1834bc0635278b0fcdb6b6b2ebe3a7fef2b8154e` (/home/pyth/rust-miniscript)

## Acceptance criteria
- Build cleanly: `just build`
- Existing tests pass: `./src/test_descriptor` and `python3 src/test/test_descriptor.py`
- Commit message follows project convention (`area: imperative summary`)
- Diff scoped strictly to this task

## Notes
See `.cm/PLAN.md` and `/home/pyth/.claude/plans/fluffy-dazzling-robin.md` for the full plan and rebase strategy.

Note: commit-hash references in this plan are stable via the original commit message attached. Hashes may have shifted under interactive rebases — match by message text rather than hash when in doubt.
