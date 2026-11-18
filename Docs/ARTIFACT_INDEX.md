# Latest Verified Frontline Artifacts

Status date: **2026-11-19**.

This index records artifacts verified in the current file workspace. It does **not** mean the binary files have been uploaded to this GitHub repository.

## Current complete source and network package

- FrontlineProtocol_v11.0.0.0_Complete_Maintenance_2026-11-19.zip — 1,432,235 bytes; 490 entries; CRC PASS; SHA-256 f9db9054d49e62c72137045848ac70af55df1a451734ad0a221d96700772a6fa.
- FrontlineProtocol_v11.0.0.0_Network_And_Runtime_Patch_Maintenance_2026-11-19.zip — 132,194 bytes; 33 entries; 31 payload files; CRC PASS; SHA-256 3b5c4be9e4909fb3756bf62c594bf3d3b0b617c5911a025dd807c1ca86637afc.
- FrontlineProtocol_v11.0.0.0_Maintenance_Update_Log_2026-11-19.docx — 39,091 bytes; SHA-256 35bb8b7a6e72bcf0e8b5c9ed044c6bc40e9d3983a08266336a8f62bfb6f1c630.
- FrontlineProtocol_Daily_Maintenance_Report_2026-11-19.docx — 41,406 bytes; SHA-256 3f960c03a1070776148580f8a45150d0a5afae05140ebd465d366c9694bceeb6.
- FrontlineProtocol_Daily_Maintenance_Evidence_2026-11-19.zip — 72,805 bytes; 47 entries; CRC PASS; SHA-256 339b07c5a4ccd9998e48ccd75773708bf5e87fdbd2d0dfd01b561cfedc6247ca.

## Maintenance result

- Latest verified complete source version: **v11.0.0.0**; v12.0.0.0 remains blocked.
- 16/16 regression entry points passed individually after metadata corrections.
- Static integrity: 488/488 integration manifest; 489/489 SHA256SUMS; 56/56 JSON; 145/145 Unity meta pairs; 145 unique GUIDs; 28 OBJ files / 928 faces / zero invalid indices; 48 C# structural checks.
- Two metadata discrepancies corrected: JSON count 54→56 and network patch payload count 30→31. metadata_hygiene_corrections = 3.
- No runtime code, config, art, API, protocol or Schema change. Formal version remains v11.0.0.0.
- The 2026-11-18 WebSocket Errata claim was withdrawn because the cited sentence is a historical v6.0.3.1 note; the current protocol section is correct.
- No Unity Editor/Play Mode/CI/APK/Android/Windows/production TLS/WSS/pressure/soak acceptance was executed.

## v12 candidate and blocker materials

Audit reports and candidate diffs are evidence only. No complete v12 Client/Hub Server/Admin source tree, 12-group art overlay or FieldOperationsCatalog_v12.json was found in the accessible file set.
