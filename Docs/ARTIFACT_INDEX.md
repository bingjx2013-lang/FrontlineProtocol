# Latest Verified Frontline Artifacts

Status date: **2026-11-17**.

This index records artifacts verified in the current file workspace. It does **not** mean the binary files have been uploaded to this GitHub repository.

## Current complete source and network baseline

- `FrontlineProtocol_v11.0.0.0_Complete.zip` — 1,432,078 bytes; 490 entries; CRC PASS; SHA-256 `a2c1e21c12e9076c96394228dfa18be07b8c9a7260183b6bda995933aa1198c9`.
- `FrontlineProtocol_v11.0.0.0_Network_And_Runtime_Patch.zip` — 132,041 bytes; 33 entries; CRC PASS; SHA-256 `0e9478cc73271e5b51106111c2b8b15347d63557bcf474224ed30331a29088d5`.
- `FrontlineProtocol_v11.0.0.0_Update_Log.docx` — 39,777 bytes; SHA-256 `a53dc56577f8eb7a7ed8fc56bf7967b1785fe51c336109c2eedd36239992cbf0`.

## Daily maintenance reports and evidence

- `FrontlineProtocol_Daily_Maintenance_Report_2026-11-15.docx` — 39,655 bytes; SHA-256 `e8bcbcf8de05c4ad9269572a26c5f5ff163e79983f4fb0a478c6f9c83cb93a50`.
- `FrontlineProtocol_Daily_Maintenance_Evidence_2026-11-15.zip` — 44,606 bytes; 8 entries; CRC PASS; SHA-256 `cb9ea540d9dc1dc6679b1cf334872b95c789ad213e408b45ca416ebd479f7f57`.
- `FrontlineProtocol_Daily_Maintenance_Report_2026-11-16.docx` — 40,440 bytes; SHA-256 `1a2b367eec7bccebc7f44b1ec4296c0e9268c757774592a7d064fac14ee0b762`.
- `FrontlineProtocol_Daily_Maintenance_Evidence_2026-11-16.zip` — 50,558 bytes; CRC PASS; SHA-256 `26aba7c5d0549f5df7dedec87038ad5f1ee0bdae4443b7bf1bef04c7f0938db4`.
- `FrontlineProtocol_Daily_Maintenance_Report_2026-11-17.docx` — 41,158 bytes; SHA-256 `dfdc9b22e5ddf261f534704bab5f2bb87c043c8c3721d2bc0a00b7f1b4822fb0`.
- `FrontlineProtocol_Daily_Maintenance_Evidence_2026-11-17.zip` — 26 entries; CRC PASS; binary remains in the ChatGPT file workspace (not uploaded to this repository).

## v12 candidate and blocker materials

The following are candidate/audit evidence only and do not establish a complete v12 source release:

- `FrontlineProtocol_v12.0.0.0_Rebase_Blocker_Report.docx`
- `FrontlineProtocol_v12.0.0.0_Candidate_Network_Source_Repair_Patch.zip`
- `CANDIDATE_SOURCE_CHANGES.diff`
- `FrontlineProtocol_v12.0.0.0_Deep_Source_Audit_Report.docx`
- `FrontlineProtocol_v12.0.0.0_Update_Log_Audit_Run.docx`
- `FrontlineProtocol_v12.0.0.0_Source_Audit_Evidence_Bundle.zip`
- `VERSION_DECISION_v12.0.0.0.md`
- `TEST_RESULTS_v12.0.0.0.txt`
- `DELIVERY_VALIDATION.json`
- `SHA256SUMS_v12.0.0.0_Audit_Run.txt`

No complete v12 Client/Hub Server/Admin source tree, 12-group art overlay, or `FieldOperationsCatalog_v12.json` was found in the current accessible file set.

## Current maintenance result

- v11.0.0.0 remains the latest verified complete source baseline.
- 16/16 regression entry points passed individually; aggregate one-shot runner was incomplete due execution-window timeout.
- Static integrity: 488/488 integration-manifest files, 489/489 SHA256SUMS, 56/56 JSON parse, 18/18 Python AST/compileall, 145/145 Unity meta pairs, 145 unique GUIDs, 28 OBJ files / 928 faces / zero invalid indices, 48 C# structural checks.
- No code/config/art/API/schema change was made; no new formal version or network patch was created.
- This repository remains a test mirror with text-only metadata; the formal main repository remains `We-MCS/Project_Frontline-Protocol`.
