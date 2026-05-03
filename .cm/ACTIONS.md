# Build and Test Actions — libwally-core

## Build Commands

### Primary Build

```bash
just build
```

This wraps `bear -- make -j$(nproc)`, regenerating `compile_commands.json` so clangd works correctly. Run after any source change.

### Just `make`

```bash
make -j$(nproc)
```

Faster (no compile_commands.json regeneration), but clangd may go stale.

## Lint Commands

The project uses uncrustify but **does not** run it on every commit. Formatting is handled in dedicated commits per the project convention. Do not run uncrustify as part of normal task verification.

```bash
# Project-managed (do NOT run during review tasks):
# tools/uncrustify
```

## Test Commands

### C tests (descriptor + miniscript)

```bash
./src/test_descriptor
```

Returns exit 0 on success.

### Python tests (descriptor + PSBT)

```bash
python3 src/test/test_descriptor.py
python3 src/test/test_psbt.py
python3 src/test/test_musig.py
```

Each prints `OK` on success.

### All tests

```bash
make check
```

Runs the full C + Python test suite.

## Verification Sequence

After each phase the agent runs:

1. **Build:** `just build` (configured in `.cm/config.toml` as `build_commands`)
2. **Tests:** `./src/test_descriptor && python3 src/test/test_descriptor.py`

Build is the gate; if it fails, the phase reverts.

## Environment Setup

No special environment variables required. Standard autotools toolchain (`autoconf`, `automake`, `libtool`, `gcc`, `make`, `bear`).

## Clean Commands

```bash
make clean        # remove built objects, keep configure output
make distclean    # remove configure output too
```

## Notes

- **`bear` is required** for `compile_commands.json` regeneration. Install via `apt install bear` or equivalent.
- **`just` is required** for `just build` (wrapper). Install via `cargo install just` or distro package.
- **secp256k1 submodule:** vendored at `src/secp256k1/` — don't run `make` inside it directly.
- **Single-threaded builds** sometimes succeed where parallel fails (autotools dependency tracking edge cases). If `make -j$(nproc)` fails inexplicably, try `make -j1`.
- **Rebase note:** every commit in the wally-miniscript-satisfier rebase MUST build cleanly. Bisectability is a hard requirement.
