# phase-2.task-1: Split de8d0d8f "descriptor: add tr() parser, taptree, and BIP-341 tweak" into 3 parts

## Goal

Split de8d0d8f "descriptor: add tr() parser, taptree, and BIP-341 tweak" into 3 parts

## Type
implement

## Status
completed

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
