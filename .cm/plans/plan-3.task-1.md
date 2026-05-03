# phase-3.task-1: Split 5e1ec21a "descriptor: add taproot leaf and key accessor APIs" into 3 parts

## Goal

Split 5e1ec21a "descriptor: add taproot leaf and key accessor APIs" into 3 parts

## Type
implement

## Status
completed

## Files to read
- `src/descriptor.c`
- `include/wally_descriptor.h`

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
