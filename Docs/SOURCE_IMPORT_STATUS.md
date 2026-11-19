# Source Import Inventory

Repository: bingjx2013-lang/FrontlineProtocol
Branch: main
Role: **user-owned test mirror; not the formal main repository**.

## Current verified source baseline — 2026-11-20

The latest complete source package verified in the current ChatGPT file workspace is a maintenance refresh of **v11.0.0.0**:

| Artifact | Size | SHA-256 | Verification |
|---|---:|---|---|
| FrontlineProtocol_v11.0.0.0_Complete_Maintenance_2026-11-20.zip | 1,517,723 bytes | ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e | 497 entries; ZIP CRC PASS |
| FrontlineProtocol_v11.0.0.0_Network_Regression_Test_Patch_2026-11-20.zip | 41,530 bytes | c4fa943e9a42f86885522aff3a1b33c067c19902454d090cc6200f0ee4a556c3 | 5 entries; ZIP CRC PASS; test-harness only |
| FrontlineProtocol_v11.0.0.0_Maintenance_Update_Log_2026-11-20.docx | 39,501 bytes | 19aad9857b38a03e0ef36997efed869c1d53412feed8067cafecd293d71c2ecf | Word update log |
| FrontlineProtocol_Daily_Maintenance_Report_2026-11-20.docx | 39,949 bytes | 36ebfcf2b0b6e7c4a01665c93fc2d51d0e435636b1659d740d367ad674f6fe56 | Word daily report |
| FrontlineProtocol_Daily_Maintenance_Evidence_2026-11-20.zip | 143,359 bytes | 02fa5c719c07173d49227933cfc469f0c7a765447401f7648709eb7541023ba5 | 19 entries; ZIP CRC PASS |

These binary artifacts are available in the current file workspace, **but are not committed to this GitHub repository**. This repository contains metadata/index text only; do not interpret this inventory as a source upload.

## 2026-11-20 maintenance reconciliation

- 16/16 regression entry points passed individually after the test-harness correction (12 self-contained + 4 isolated-server).
- The corrected `maintenance_regression_test.py` passed five additional consecutive standalone runs.
- The original test read only the next WebSocket frame after sending a command; a periodic `snapshot` could arrive first. The test now skips only snapshot frames while waiting for the expected response, with a five-second deadline. Other unexpected events still fail.
- Runtime source/config/art/API/protocol/Schema unchanged. This is not a runtime bug fix and does not increment the formal version.
- Python compileall: 18 files, exit code 0. JSON: 57/57 parse.
- Unity .meta: 145/145 pairs; 145 unique GUIDs. OBJ: 28 files, 1,320 vertices, 928 faces, zero invalid indices. C# delimiter scan: 48 files; not a C# compile.
- INTEGRATION_MANIFEST: 495/495 exact; SHA256SUMS: 496/496 exact.
- Version markers in Client, Unity bundle, Hub Server config, Admin Panel and PowerShell script remain v11.0.0.0.
- Aggregate `Tests/run_regression_suite.py` exceeded the 300-second execution window; the 16/16 count is based on individual entry-point results, not a completed aggregate run.
- Unity Editor, Play Mode, CI, APK/AAB, Android device, Windows host, production TLS/WSS, pressure/soak acceptance were not executed.

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
