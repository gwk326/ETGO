# ETGO source

The complete **published code snapshot** is provided as the versioned ZIP in this repository’s Releases section. Download and extract that ZIP to obtain the `source/` tree, build scripts and tests described below. The repository root contains the publication documents and manifests. The published snapshot is code-only; the full-installer gaps below remain open.

## ETGO 2.1.4-rc3

Source-code publication prepared 5 October 2026. ETGO is a modified ET:Legacy / Wolfenstein: Enemy Territory project.

This snapshot preserves the RC3 gameplay, UI and Linux dedicated-server code, native launcher and data-helper source, build/install/update scripts, tests, vendored source dependencies, and the historical source overlay supplied for the retained Windows engine. Original notices remain intact. ETGO changes include one-life rounds, class/loadout UI, matchmaking/admission, public team capacity and bot integration, results/map voting, and installer/update tooling.

## License and scope

The main ET:Legacy/ETGO code is GPL-3.0-or-later with the additional id Software terms in [COPYING.txt](COPYING.txt). Individual files and third-party components retain their own notices. Read [LICENSE-NOTICE.md](LICENSE-NOTICE.md) before redistribution. No trademark license or upstream endorsement is claimed.

This is a source-code snapshot, not a standalone game. Compiled releases, the separate Omni-bot runtime, most game media, community maps and original ET data are not included. ETGO branding inputs and generated resources used by the included code are retained. See [PUBLICATION-MANIFEST.json](PUBLICATION-MANIFEST.json) for the exact file boundary.

This publication is a step toward fulfilling source-distribution obligations. It does **not yet establish complete corresponding source or redistribution clearance for every component of the full RC3 installer**. The retained Windows engine recipe/dependencies, certain third-party notices, and excluded script/asset preferred forms still require review. See [SOURCE-STATUS.md](SOURCE-STATUS.md).

## Build and verify

See [BUILD.md](BUILD.md) for native module builds and limitations. `source/` contains the project and vendored dependencies; its nested `.gitmodules` is retained historical upstream metadata, not a request to replace the vendored libraries with current branches.

[PUBLICATION-SHA256SUMS.txt](PUBLICATION-SHA256SUMS.txt) records this published snapshot. The historical `Source-SHA256SUMS.txt` and other RC3 build records describe the original full bundle, including omitted files; they are preserved as evidence and are not a checksum command for this filtered tree.

The original canonical RC3 game archive was `etgo_2.1.4-rc3.pk3`, SHA-256 `5dc2aa924771f25cd904b53c4ab311911bcba0114e2c4120f507aeb7b8e2f975`. It is not republished here. Source contents copied from that release remain byte-identical; publication documentation and the missing LuaSQL license notice are additional files.

When distributing binaries, provide clear directions beside each binary download to the source for that exact release, including its build instructions and any required additional corresponding source. Linking only a moving development branch is not an exact-version source record. See the [GNU source-distribution FAQ](https://www.gnu.org/licenses/gpl-faq.en.html#SourceAndBinaryOnDifferentSites).
