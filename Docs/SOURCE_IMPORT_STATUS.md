# Source Import Inventory

Repository: `bingjx2013-lang/FrontlineProtocol`
Branch: `main`
Role: **user-owned test mirror; not the formal main repository**.

## Current verified source baseline — 2026-11-17

The latest complete source archive verified in the current ChatGPT file workspace is **v11.0.0.0**:

| Artifact | Size | SHA-256 | Verification |
|---|---:|---|---|
| `FrontlineProtocol_v11.0.0.0_Complete.zip` | 1,432,078 bytes | `a2c1e21c12e9076c96394228dfa18be07b8c9a7260183b6bda995933aa1198c9` | 490 entries; ZIP CRC PASS |
| `FrontlineProtocol_v11.0.0.0_Network_And_Runtime_Patch.zip` | 132,041 bytes | `0e9478cc73271e5b51106111c2b8b15347d63557bcf474224ed30331a29088d5` | 33 entries; ZIP CRC PASS |
| `FrontlineProtocol_v11.0.0.0_Update_Log.docx` | 39,777 bytes | `a53dc56577f8eb7a7ed8fc56bf7967b1785fe51c336109c2eedd36239992cbf0` | File fingerprint verified |

These binary artifacts are available in the current file workspace, **but are not committed to this GitHub repository**. This repository currently contains metadata/index text only; do not interpret this inventory as a source upload.

## Correction to the 2026-11-15 import note

The earlier note below stated that only a v10.0.0.2 archive was locally materialized. That statement is superseded by the later verified v11.0.0.0 file-workspace artifacts listed above. The correct current status is: v11 binaries are available in the file workspace and verified, but have not been committed as GitHub binary files.

## v12.0.0.0 status

**BLOCKED — no complete v12 source baseline is currently accessible.**

The current conversation files and the five-page Library inventory (475 items scanned) did not contain:
- Complete v12 Client source and Unity project settings/packages;
- Hub Server (枢纽) source;
- Admin/AdminPanel source tree;
- The 12-group art overlay with OBJ, Prefab, materials/textures and matching `.meta/GUID`;
- `FieldOperationsCatalog_v12.json`;
- A complete v12 VERSION, BUG_FIX_COUNTER, BUG_REGISTER, INTEGRATION_MANIFEST and SHA256SUMS set.

Candidate diffs and blocker/audit documents are not a substitute for a complete v12 source tree. A candidate patch that was checked against v11 is not thereby validated against v12.

## GitHub repository status

- Formal main repository: `We-MCS/Project_Frontline-Protocol`; main contains only README, repository size is 0 KB, and the current connector permission is pull=true / push=false.
- This test mirror: main contains README and text-only VERSION/Docs records; no `server.py` or `FrontlineClientBootstrap` source was found.
- No complete source archive has been committed to either repository in this maintenance run.

## 2026-11-17 maintenance reconciliation

- v11 regression entry points: 16/16 passed individually (12 self-contained + 4 isolated-server tests); aggregate one-shot runner remained incomplete due execution-window timeout.
- Static checks: 488/488 integration-manifest files and 489/489 SHA256SUMS entries match; 56 JSON files parse; 18 Python files pass AST/compileall; 145/145 Unity asset/meta pairs and 145 unique GUIDs; 28 OBJ files with 928 faces and zero invalid face indices; 48 C# files pass structural delimiter checks (not compilation).
- A metadata discrepancy was found: v11 MAINTENANCE_STATUS and VALIDATION_REPORT say 54 JSON files; the fresh package scan found 56. The published v11 package was left immutable; the discrepancy is recorded for the next formal package revision.
- Formal version remains v11.0.0.0; no source, config, art, API or schema changes were made.

## Required next import

Upload the verified v11 binaries to this repository through GitHub's web UI or a Git-capable client if repository mirroring is desired. For a v12 release, first restore the complete v12 source tree, art overlay and version/bug/integration manifests, then run the full source rebase and cross-module validation. Do not label this test mirror as the formal main repository.


## 2026-11-18 maintenance reconciliation

- Rechecked the formal repository `We-MCS/Project_Frontline-Protocol`: branch `main`, size 0 KB, README only; current connector permission is pull=true / push=false. The latest accessible commit is `d5fd155bdb482125b98d169a9a81d458de0c9180` (Initial commit, 2026-11-15T00:10:18Z).
- This test mirror remains text-only metadata/index documentation, not the formal main repository. Its current main head before this maintenance record was `ed1ad1140b404d749f88960cc88b83048dfaf9e0`.
- v11.0.0.0 complete archive and network patch were rechecked from the current file workspace. Complete ZIP: 1,432,078 bytes, 490 entries, CRC PASS, SHA-256 `a2c1e21c12e9076c96394228dfa18be07b8c9a7260183b6bda995933aa1198c9`. Network patch: 132,041 bytes, 33 entries, CRC PASS, all 33 entries byte-identical to corresponding files in the complete archive.
- 16/16 regression entry points passed individually (12 self-contained + 4 isolated-server). The aggregate one-shot runner exceeded the 300-second command window and remains TIMEOUT, not PASS.
- Static checks: integration manifest 488/488 exact; SHA256SUMS 489/489 exact; 56/56 JSON parse; Python compileall 18/18; Unity .meta pairs 145/145 with unique GUIDs; OBJ 28 files / 1,320 vertices / 928 faces / zero invalid indices; C# 48 files passed delimiter scan only (not compilation).
- Two documentation discrepancies were recorded in `Docs/ERRATA_v11.0.0.0_2026-11-18.md`: Server/README.md still says WebSocket query-string tokens are used, while current tests confirm Authorization: Bearer and query-token rejection; v11 validation/status documents say 54 JSON files, while the archive contains 56 and all parse.
- No source, configuration, art, API, protocol, or Schema changes were made. Formal version remains v11.0.0.0. No new complete project ZIP or network patch was generated.
- v12.0.0.0 remains BLOCKED: complete Client/Hub Server/Admin source, 12-group art overlay, FieldOperationsCatalog_v12.json and version/bug/integration manifests are not accessible.
- Unity Editor, Play Mode, CI, APK/AAB, Android device, Windows host, production TLS/WSS and pressure/soak acceptance were not executed.
