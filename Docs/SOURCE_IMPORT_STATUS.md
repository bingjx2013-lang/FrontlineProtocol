# Source Import Inventory

Repository: bingjx2013-lang/FrontlineProtocol
Branch: main
Role: **user-owned test mirror; not the formal main repository**.

## Current verified source baseline — 2026-11-22

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


## 2026-11-22 verification — run 8

- The latest complete source package remains `FrontlineProtocol_v11.0.0.0_Complete_Maintenance_2026-11-20.zip` (1,517,723 bytes; 497 entries; CRC PASS; SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`).
- 12/12 self-contained and 4/4 isolated-server regression entries passed individually; maintenance regression repeated 5/5; admin cookie probes 3/3.
- Aggregate runner did not return a final summary after two time-limited attempts; status INCOMPLETE, not PASS. QA-AGG-001 is a test-harness/orchestration observation, not a runtime bug.
- Static integrity: integration 495/495; SHA256SUMS 496/496; JSON 57/57; Python compileall 18 files; Unity .meta 145/145 and 145 unique GUIDs; OBJ 28 / 1,320 vertices / 928 faces / 0 invalid indices; C# lexical scan 48 files (not compilation).
- Client, Unity bundleVersion, Hub config, Admin Panel and PowerShell banner agree on v11.0.0.0; API Schema v1; Realtime Protocol v1.
- `admin_cookie_secure=false` remains the documented local HTTP default; direct Secure config and trusted proxy HTTPS header probes passed. Production TLS/WSS remains untested.
- No source/runtime/config/art/API/protocol/Schema changes; no version increment; runtime bug counts new/fixed/open = 0/0/0.
- Run 8 daily report: 40,342 bytes, SHA-256 `9ae526e2388a3391bd692932928621074478bce474b3ad58f1a7053fa83e3b57`.
- Run 8 no-code update log: 38,189 bytes, SHA-256 `5f6b7e5dd8e177a28475433fef5044dc5d6d95c179544f2d2c79f2dad442c7bc`.
- Run 8 evidence ZIP: 16 entries, CRC PASS, SHA-256 `c180d33275943b6cccbdf3563ae950e82a6de4c9ef256d488304bc14c4504067`.

## Current GitHub source import status — 2026-11-22

- Formal main repository `We-MCS/Project_Frontline-Protocol`: one 28-byte README, size 0 KB, current connection `pull=true / push=false`.
- Legacy `We-MCS/Frontline-Protocol`: one 3-byte source stub in its recursive tree.
- This test mirror contains 15 text/documentation entries only; no Client/Server/Admin source tree. Binary artifacts remain in the ChatGPT file workspace and are not committed here.

