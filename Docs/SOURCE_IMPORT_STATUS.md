# Source Import Inventory

Repository: bingjx2013-lang/FrontlineProtocol
Branch: main
Role: **user-owned test mirror; not the formal main repository**.

## Current verified source baseline — 2026-11-21

The latest complete source package verified in the current ChatGPT file workspace remains a maintenance refresh of **v11.0.0.0**, dated 2026-11-20.

| Artifact | Size | SHA-256 | Verification |
|---|---:|---|---|
| FrontlineProtocol_v11.0.0.0_Complete_Maintenance_2026-11-20.zip | 1,517,723 bytes | ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e | 497 entries; ZIP CRC PASS |
| FrontlineProtocol_v11.0.0.0_Network_Regression_Test_Patch_2026-11-20.zip | 41,530 bytes | c4fa943e9a42f86885522aff3a1b33c067c19902454d090cc6200f0ee4a556c3 | 5 entries; ZIP CRC PASS; test-harness only |
| FrontlineProtocol_v11.0.0.0_Maintenance_Update_Log_2026-11-20.docx | 39,501 bytes | 19aad9857b38a03e0ef36997efed869c1d53412feed8067cafecd293d71c2ecf | Word update log |
| FrontlineProtocol_Daily_Maintenance_Report_2026-11-20.docx | 39,949 bytes | 36ebfcf2b0b6e7c4a01665c93fc2d51d0e435636b1659d740d367ad674f6fe56 | Word daily report |
| FrontlineProtocol_Daily_Maintenance_Evidence_2026-11-20.zip | 143,359 bytes | 02fa5c719c07173d49227933cfc469f0c7a765447401f7648709eb7541023ba5 | 19 entries; ZIP CRC PASS |

These binary artifacts are available in the current file workspace, **but are not committed to this GitHub repository**. This repository contains metadata/index text only; do not interpret this inventory as a source upload.

## 2026-11-21 verification

- 16/16 regression entry points passed individually (12 self-contained + 4 isolated-server); corrected maintenance regression passed five additional consecutive runs (5/5).
- Aggregate `Tests/run_regression_suite.py` did not complete within 300 seconds and emitted no final summary; recorded INCOMPLETE, not PASS.
- Complete ZIP: 497 entries, CRC PASS. Test-only patch ZIP: 5 entries, CRC PASS; sole payload byte-identical to the full package.
- INTEGRATION_MANIFEST: 495/495 exact. SHA256SUMS: 496/496 exact.
- 57 JSON files parsed successfully: 56 project JSON files plus the integration manifest itself.
- Python compileall: 18 files, exit 0. Unity .meta: 145/145 pairs, 145 unique GUIDs. OBJ: 28 files, 1,320 vertices, 928 faces, zero invalid indices. C# structural scan: 48 files; not a C# compile.
- Client VERSION, Unity bundleVersion, Hub Server config, Admin Panel banner, PowerShell setup banner and VERSION.md all agree on v11.0.0.0.
- No project source/runtime/config/art/API/protocol/Schema change this run; formal version remains v11.0.0.0; runtime bug counts new/fixed/open = 0/0/0.
- The 2026-11-20 patch is test-harness only, not a runtime network patch. The 2026-11-19 package remains the latest runtime network patch.
- Daily report: FrontlineProtocol_Daily_Maintenance_Report_2026-11-21.docx, 40,802 bytes, SHA-256 5a198d1cc98d691c04bcaa03e0677f5667833a93d1a6af2093b220fa06321835.
- No-code-change update log: FrontlineProtocol_v11.0.0.0_Maintenance_No_Code_Change_Log_2026-11-21.docx, 38,765 bytes, SHA-256 8940cbf73f517325d5023f4d111c5d6db6e7219f77ed14cf700cca80943130fd.
- Evidence ZIP: FrontlineProtocol_Daily_Maintenance_Evidence_2026-11-21.zip, 26 entries, CRC PASS, SHA-256 4d4ecd5856d28243b3be082e4c1c22829b40e2b8063fb543834d343480e94b7f.

## GitHub repository status

- Formal main repository: We-MCS/Project_Frontline-Protocol; main contains only README.md, size 0 KB, current connector permission pull=true / push=false.
- This test mirror remains text-only. No complete source archive has been committed to either repository in this run.

## v12.0.0.0 status

**BLOCKED — no complete v12 source baseline is currently accessible.** Missing inputs remain:
- Complete v12 Client, Hub Server (枢纽), Admin/AdminPanel source tree;
- 12-group art overlay with OBJ, Prefab, materials/textures and matching .meta/GUID;
- FieldOperationsCatalog_v12.json;
- v12 VERSION, BUG_FIX_COUNTER, BUG_REGISTER, INTEGRATION_MANIFEST and SHA256SUMS.

Candidate diffs and audit reports are not substitutes for a complete v12 source tree.
