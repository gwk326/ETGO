# Source publication status

Prepared 2026-10-05 for ETGO 2.1.4-rc3.

## Preserved

Current native source, build/install/update scripts, tests, vendored library source and notices, version/build/PK3 records, generated version headers, and the old Windows-engine source restoration overlay. Existing included source files are unchanged from the frozen RC3 bundle. Publication documents and LuaSQL's missing notice are new.

## Open before claiming complete corresponding source for the entire installer

1. Verify the exact retained Windows engine/renderer build options, dependency versions, local modifications, and corresponding dependency-source availability. The source overlay exists, but the supplied mod recipe does not prove engine rebuild completeness.
2. Resolve the anti-wallhack GPLv2-only-looking header and the inherited Omni-bot SDK/runtime licensing boundary.
3. Resolve rights and preferred source forms for excluded bot overlays, player presets and game assets. Excluding a file from this repository does not erase obligations if it was already conveyed in a binary package.
4. Complete asset/runtime license and attribution review before any additional public binary/media redistribution.
5. Put clear exact-version source directions alongside every binary distribution and maintain the required availability. A repository alone is not a compliance guarantee.

## File boundaries

PUBLICATION-MANIFEST.json lists original-bundle files included and excluded with their hashes and reasons. Compiled output, frozen runtime content, third-party media and unneeded historical build logs are omitted. The original complete-bundle hash list remains as historical evidence and includes excluded entries.

The source snapshot can be inspected and modified, and current native module build scripts are supplied. Complete game/installer packaging needs separately cleared missing inputs. Existing release QA limits remain in VALIDATION.txt; no full Windows gameplay, public 20v20 load or clean-download acceptance is claimed by this publication.

## Local publication-snapshot check

On 5 October 2026, the filtered snapshot successfully rebuilt Linux x86_64 qagame, UI and cgame using the supplied configure-linux.sh, CMake and native toolchain. All included original-source hashes were unchanged by that build. This is compilation evidence only, not game/runtime acceptance or verification of every historical binary/dependency.
