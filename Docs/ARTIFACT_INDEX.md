# Latest Verified Frontline Artifacts

Status date: **2026-11-20**.

This index records artifacts verified in the current file workspace. It does **not** mean the binary files have been uploaded to this GitHub repository.

## Current complete source and test patch

- FrontlineProtocol_v11.0.0.0_Complete_Maintenance_2026-11-20.zip — 1,517,723 bytes; 497 entries; CRC PASS; SHA-256 ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e.
- FrontlineProtocol_v11.0.0.0_Network_Regression_Test_Patch_2026-11-20.zip — 41,530 bytes; 5 entries; CRC PASS; SHA-256 c4fa943e9a42f86885522aff3a1b33c067c19902454d090cc6200f0ee4a556c3.
- FrontlineProtocol_v11.0.0.0_Maintenance_Update_Log_2026-11-20.docx — 39,501 bytes; SHA-256 19aad9857b38a03e0ef36997efed869c1d53412feed8067cafecd293d71c2ecf.
- FrontlineProtocol_Daily_Maintenance_Report_2026-11-20.docx — 39,949 bytes; SHA-256 36ebfcf2b0b6e7c4a01665c93fc2d51d0e435636b1659d740d367ad674f6fe56.
- FrontlineProtocol_Daily_Maintenance_Evidence_2026-11-20.zip — 143,359 bytes; 19 entries; CRC PASS; SHA-256 02fa5c719c07173d49227933cfc469f0c7a765447401f7648709eb7541023ba5.

## Maintenance result

- Latest verified complete source version: **v11.0.0.0**; v12.0.0.0 remains blocked.
- 16/16 regression entry points passed individually after the WebSocket test-harness correction; five additional consecutive runs of the corrected maintenance test passed.
- Static integrity: 495/495 integration manifest; 496/496 SHA256SUMS; 57/57 JSON; 145/145 Unity meta pairs; 145 unique GUIDs; 28 OBJ files / 1,320 vertices / 928 faces / zero invalid indices; 48 C# delimiter checks.
- The maintenance patch corrects a test-only race caused by periodic WebSocket snapshots. Runtime source, config, art, API, protocol and Schema did not change.
- Formal version remains v11.0.0.0; runtime bug counts new/fixed/open remain 0/0/0.
- No Unity Editor/Play Mode/CI/APK/Android/Windows/production TLS/WSS/pressure/soak acceptance was executed.
- No binary archive has been uploaded to GitHub. The formal main repository is not writable through the current connector; this test mirror contains text records only.

## v12 candidate and blocker materials

No complete v12 Client/Hub Server/Admin source tree, 12-group art overlay or FieldOperationsCatalog_v12.json was found in the accessible file set.
