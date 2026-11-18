# Source Import Inventory

Repository: bingjx2013-lang/FrontlineProtocol
Branch: main
Role: **user-owned test mirror; not the formal main repository**.

## Current verified source baseline — 2026-11-19

The latest complete source package verified in the current ChatGPT file workspace is a documentation/metadata maintenance refresh of **v11.0.0.0**:

| Artifact | Size | SHA-256 | Verification |
|---|---:|---|---|
| FrontlineProtocol_v11.0.0.0_Complete_Maintenance_2026-11-19.zip | 1,432,235 bytes | f9db9054d49e62c72137045848ac70af55df1a451734ad0a221d96700772a6fa | 490 entries; ZIP CRC PASS |
| FrontlineProtocol_v11.0.0.0_Network_And_Runtime_Patch_Maintenance_2026-11-19.zip | 132,194 bytes | 3b5c4be9e4909fb3756bf62c594bf3d3b0b617c5911a025dd807c1ca86637afc | 33 entries; 31 payload files; ZIP CRC PASS |
| FrontlineProtocol_v11.0.0.0_Maintenance_Update_Log_2026-11-19.docx | 39,091 bytes | 35bb8b7a6e72bcf0e8b5c9ed044c6bc40e9d3983a08266336a8f62bfb6f1c630 | Word update log |
| FrontlineProtocol_Daily_Maintenance_Report_2026-11-19.docx | 41,406 bytes | 3f960c03a1070776148580f8a45150d0a5afae05140ebd465d366c9694bceeb6 | Word daily report |
| FrontlineProtocol_Daily_Maintenance_Evidence_2026-11-19.zip | 72,805 bytes | 339b07c5a4ccd9998e48ccd75773708bf5e87fdbd2d0dfd01b561cfedc6247ca | 47 entries; CRC PASS |

These binary artifacts are available in the current file workspace, **but are not committed to this GitHub repository**. This repository contains metadata/index text only; do not interpret this inventory as a source upload.

## 2026-11-19 maintenance reconciliation

- 16/16 regression entry points passed individually after the metadata corrections (12 self-contained + 4 isolated-server).
- Python compileall: 18 source files; exit code 0. JSON: 56/56 parse. Unity .meta: 145/145 pairs; 145 unique GUIDs. OBJ: 28 files, 1,320 vertices, 928 faces, zero invalid indices. C# structural delimiter scan: 48 files, no structural errors; this is not C# compilation.
- INTEGRATION_MANIFEST: 488/488 exact; SHA256SUMS: 489/489 exact.
- Corrected two metadata count errors: JSON inventory 54→56; network patch payload 30→31. The patch contains 31 payload files plus PATCH_MANIFEST and PATCH_SHA256SUMS, totaling 33 entries.
- metadata_hygiene_corrections counter is now 3; runtime bug new/fixed/open remain 0.
- The prior 2026-11-18 WebSocket Errata classification is withdrawn: the query-token sentence is in the v6.0.3.1 historical section. The current protocol section, server implementation and regression tests consistently require Authorization: Bearer and reject query tokens.
- No runtime source, config, art, API, protocol or Schema changed. Formal version remains **v11.0.0.0**.
- Unity Editor, Play Mode, CI, APK/AAB, Android device, Windows host, production TLS/WSS and pressure/soak acceptance were not executed.

## GitHub repository status

- Formal main repository: We-MCS/Project_Frontline-Protocol; main contains only README, size 0 KB, current connector permission pull=true / push=false.
- This test mirror remains text-only. No complete source archive has been committed to either repository in this run.

## v12.0.0.0 status

**BLOCKED — no complete v12 source baseline is currently accessible.** Missing inputs remain:
- Complete v12 Client, Hub Server (枢纽), Admin/AdminPanel source tree;
- 12-group art overlay with OBJ, Prefab, materials/textures and matching .meta/GUID;
- FieldOperationsCatalog_v12.json;
- v12 VERSION, BUG_FIX_COUNTER, BUG_REGISTER, INTEGRATION_MANIFEST and SHA256SUMS.

Candidate diffs and audit reports are not substitutes for a complete v12 source tree.
