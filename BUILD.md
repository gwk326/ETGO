# Building the published source

## Current native modules

Requirements: CMake 3.31+, Make, Python 3, a native C/C++ compiler (the release used GCC 14.2.0), GNU binutils, and Linux libcurl development headers/library. Windows cross-builds use the official Zig 0.15.2 executable. No account credentials are required.

From this repository's root:

```sh
ETGO_CMAKE=/path/to/cmake ETGO_JOBS=4 bash configure-linux.sh
ETGO_ZIG=/path/to/zig ETGO_CMAKE=/path/to/cmake ETGO_JOBS=4 bash configure-windows.sh
```

These scripts build `qagame`, `cgame`, and `ui` for Linux x86_64 and Windows x86/x64. Outputs are under `builds/`. The Windows build does not establish native Windows runtime acceptance.

`build-public-linux.sh` preserves the Linux dedicated-engine build and its regression entry points. Its engine build can run independently of complete game packaging; some asset-dependent tests need excluded release inputs. The old engine anti-wallhack license notice requires clarification before a combined-binary license-clearance claim (see LICENSE-NOTICE.md).

## Retained Windows engine

The release retained older Windows engine/renderer binaries. `source/retained-engine-build/SOURCE-RELATIONSHIP.json` describes reconstructing their supplied historical source: in a fresh copy only, overlay each listed `baseline-files` member and remove the listed RC3 additions. Never apply it to the current source in place.

The supplied historical `configure-builds-used.sh` records a mod configuration, with old local paths. It is **not a verified, complete build recipe for the retained engine/renderer executables**. Exact engine configuration and dynamically/downloaded dependency inputs still need to be recovered and verified. Android build completeness is also unverified; its joystick submodule and Gradle wrapper binary are not supplied by this snapshot.

## Packaging and assets

`package-pk3.py` and the installer/update scripts remain intact. Their full recorded media, runtime and frozen binary inputs are deliberately excluded, so the exact RC3 PK3 and complete installer cannot be regenerated from this source-only snapshot alone. Obtain and clear the matching inputs before packaging; do not weaken hash guards or replace them with unrelated files. NSIS 3.11 and Python 3 are the recorded installer tools.

Brand regeneration uses `source/tools/etgo/prepare-brand-assets.py` and Pillow, with the original `source/etmain/gfx/etgo/logo.png` included. Original derived resource bytes are retained.

The existing `VALIDATION.txt` documents the original release's testing and what was not tested. Historical build results do not certify a new rebuild. Compiler dates, generated metadata and timestamps can change output hashes; complete source still needs the actual source, dependencies and scripts used.
