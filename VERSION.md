# Frontline Protocol Version Baseline

- Formal release version: **v11.0.0.0** (A=11, B=0, C=0, D=0).
- Latest verified complete package in the ChatGPT file workspace: **v11.0.0.0 maintenance refresh, 2026-11-20**.
- Complete package: FrontlineProtocol_v11.0.0.0_Complete_Maintenance_2026-11-20.zip
- Size: 1,517,723 bytes; 497 ZIP entries; CRC PASS.
- SHA-256: ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e
- Network regression test patch: FrontlineProtocol_v11.0.0.0_Network_Regression_Test_Patch_2026-11-20.zip
- Size: 41,530 bytes; 5 ZIP entries; CRC PASS.
- Patch SHA-256: c4fa943e9a42f86885522aff3a1b33c067c19902454d090cc6200f0ee4a556c3
- Update log: 39,501 bytes; SHA-256 19aad9857b38a03e0ef36997efed869c1d53412feed8067cafecd293d71c2ecf
- Daily report 2026-11-20: 39,949 bytes; SHA-256 36ebfcf2b0b6e7c4a01665c93fc2d51d0e435636b1659d740d367ad674f6fe56
- Evidence archive 2026-11-20: 143,359 bytes; 19 entries; CRC PASS; SHA-256 02fa5c719c07173d49227933cfc469f0c7a765447401f7648709eb7541023ba5
- Last verification: **2026-11-22**. The 2026-11-20 complete package was rechecked: 16/16 regression entries passed individually; maintenance regression repeated 5/5; 495/495 integration manifest, 496/496 SHA256SUMS, 57/57 total JSON parse, 145/145 Unity meta pairs, 28 OBJ with zero invalid indices, 48 C# structural scans, and 18 Python files compileall passed.
- Aggregate Tests/run_regression_suite.py did not complete within the 300-second execution window; it is INCOMPLETE, not PASS. All 16 entries were run individually.
- No project source/config/art/API/protocol/Schema change was made on 2026-11-21. No new complete project package or runtime network patch was created. Formal version remains v11.0.0.0.
- The 2026-11-20 patch is test-harness only, not a runtime network patch. The 2026-11-19 package remains the latest runtime network patch.
- These binary artifacts are available in the ChatGPT file workspace, **not committed to this GitHub repository**. This repository remains a text-only test mirror.
- Current v12 status: **BLOCKED** — complete v12 Client/Hub Server/Admin source tree, 12-group art overlay, FieldOperationsCatalog_v12.json and v12 manifests are not accessible.
- Do not promote v11 or a candidate patch as a completed v12 release.


## 2026-11-21 follow-up run 7
- Regression: 12 self-contained + 4 isolated-server entry points = **16/16 individually PASS**; maintenance regression repeated **5/5 PASS**.
- One-shot aggregate runner remains **INCOMPLETE** because no final summary returned in the available execution window; this is not classified as PASS or FAIL.
- Static recheck: 497-entry complete ZIP CRC PASS; 495/495 integration manifest; 496/496 SHA256SUMS; JSON 57/57; Python compileall 18 files; Unity .meta 145/145 and unique GUIDs; OBJ 28 files with zero invalid indices; C# 48-file string/comment-aware delimiter scan balanced (not compilation).
- No source/runtime/config/art/API/protocol/Schema change; runtime bug counts new/fixed/open remain 0/0/0; formal version remains **v11.0.0.0**.
- Follow-up report: `FrontlineProtocol_Daily_Maintenance_Followup_2026-11-21_Run7.docx` — 39,255 bytes; SHA-256 `ee8afedcdf74827518a7a247bfb9247bae5e1d2cd83a423d957af1fec6884115`.
- No-code update log: `FrontlineProtocol_v11.0.0.0_No_Code_Change_Update_Log_2026-11-21_Run7.docx` — 37,858 bytes; SHA-256 `9ce0598e1125fe09e68a37307e94e46d626d39a84b4445474aa24a0960863562`.
- Evidence archive: `FrontlineProtocol_Daily_Maintenance_Evidence_2026-11-21_Run7.zip` — 90,810 bytes; 19 entries; CRC PASS; SHA-256 `fa760953991c4d6acdbd882052f9cd36ef0bb2584f42907d8a5f1c3e645f6c94`.
- v12.0.0.0 remains blocked by missing complete source, art overlay and manifests.


## 2026-11-22 daily maintenance run 8
- Regression: 12/12 self-contained + 4/4 isolated-server entries PASS; maintenance regression repeated 5/5; admin cookie probes 3/3.
- Aggregate runner: INCOMPLETE after two time-limited attempts; individual test entries were verified independently. Tracked as QA-AGG-001, not a runtime bug.
- Static integrity: complete ZIP 497 entries CRC PASS; integration manifest 495/495; SHA256SUMS 496/496; JSON 57/57; Python 18 files compileall; Unity .meta 145/145 with unique GUIDs; OBJ 28 files / 1,320 vertices / 928 faces / zero invalid indices; C# 48-file lexical structure scan (not compilation).
- Admin cookie behavior: local HTTP default, Secure configuration, and trusted reverse-proxy HTTPS header probes all PASS. Production TLS/WSS remains untested.
- No project source/runtime/config/art/API/protocol/Schema change; runtime bug counts new/fixed/open remain 0/0/0; formal version remains **v11.0.0.0**.
- Daily report: 40,342 bytes; SHA-256 `9ae526e2388a3391bd692932928621074478bce474b3ad58f1a7053fa83e3b57`.
- No-code update log: 38,189 bytes; SHA-256 `5f6b7e5dd8e177a28475433fef5044dc5d6d95c179544f2d2c79f2dad442c7bc`.
- Evidence archive: 84,395 bytes; 16 entries; CRC PASS; SHA-256 `c180d33275943b6cccbdf3563ae950e82a6de4c9ef256d488304bc14c4504067`.
- v12.0.0.0 remains blocked by missing complete source tree, 12-group art overlay, FieldOperationsCatalog_v12.json and v12 manifests.


## 2026-11-23 periodic source audit — run 9
- The current conversation workspace contains a v11.0.0.1 candidate complete package (1,576,260 bytes; 508 entries; CRC PASS; SHA-256 c918f99eb4370cc0814bea415a88761907597303d01b7b937a554c30444a243d) and its runtime network patch (133,688 bytes; 30 entries; CRC PASS; SHA-256 995e06544b226c842b738653dc0354d2674d3b9ec7910060689342dfa432f499).
- Candidate regression suite: 17/17 PASS; Python compileall/AST 19/19; JSON 61/61; integration manifest 506/506; SHA256SUMS 507/507; Unity .meta 145/145; OBJ 28 with zero invalid indices; C# 48-file lexical scan (not compilation); admin cookie probes 3/3.
- Baseline conflict remains: run 8 above records formal v11.0.0.0 and a 2026-11-20 497-entry complete package (SHA-256 ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e), but that binary is not accessible in the current file workspace/Library. The available v11.0.0.1 package is based on the 2026-11-15 490-entry v11.0.0.0 baseline; its rebase status against the 11/20 refresh cannot be confirmed.
- Therefore formal version remains v11.0.0.0 per the latest repository record; v11.0.0.1 is retained as a verified candidate only. No v11.0.0.2 is created. Runtime bug counts new/fixed/open this run = 0/0/0.
- Formal main repository remains README-only and push=false; no binary source or patch has been committed. This mirror update is documentation-only.
- v12.0.0.0 remains BLOCKED by missing complete Client/Hub Server/Admin source, 12-group art overlay, FieldOperationsCatalog_v12.json and manifests.


## 2026-11-23 follow-up execution — run 9
- Formal version remains **v11.0.0.0**; no code/config/art/API/protocol/Schema change was made.
- Current accessible complete archive: 2026-11-20 v11.0.0.0, 497 entries, CRC PASS, SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`.
- The v11.0.0.1 candidate mentioned in the prior source audit could not be retrieved in this execution and has not been reconciled with the 2026-11-20 archive. Do not promote it or create v11.0.0.2 yet.
- 16/16 individual regression entries PASS; admin cookie probes 3/3 PASS. Static integrity 495/495 integration, 496/496 hashes, 57 JSON, 18 Python, 145 .meta GUIDs, 28 OBJ and 48 C# lexical scans passed (C# scan is not compilation).
- Runtime bug counter new/fixed/open = 0/0/0. v12.0.0.0 remains BLOCKED by missing source, 12-group art overlay, catalog and manifests.
