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



## 2026-11-23 source audit — run 9
- Current conversation workspace candidate: v11.0.0.1 complete ZIP, 1,576,260 bytes, 508 entries, CRC PASS, SHA-256 c918f99eb4370cc0814bea415a88761907597303d01b7b937a554c30444a243d.
- Runtime network patch: 133,688 bytes, 30 entries, CRC PASS, SHA-256 995e06544b226c842b738653dc0354d2674d3b9ec7910060689342dfa432f499.
- Regression 17/17 PASS; Python 19/19 compileall + AST; JSON 61/61; integration manifest 506/506; SHA256SUMS 507/507; Unity .meta 145/145 with unique GUIDs; OBJ 28 / 1,320 vertices / 928 faces / zero invalid indices; C# lexical scan 48 files (not compilation); client/server route parity 11/11; admin cookie probes 3/3.
- Candidate source scope: 48 C# files, 19 Python files, two Web AdminPanel HTML files, 145 Unity asset/meta pairs, 28 OBJ files. No separate Android Admin project found.
- Version provenance conflict: run 8 points to a 2026-11-20 v11.0.0.0 497-entry complete archive (SHA-256 ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e), but that archive is not currently accessible. The available v11.0.0.1 candidate is based on the 2026-11-15 490-entry v11.0.0.0 baseline; do not promote it to the formal latest baseline until the 11/20 package is restored and compared.
- No new runtime source fix; bug counts new/fixed/open = 0/0/0; no version increment.
- Risks: production TLS/Secure Cookie not verified; no port fallback/discovery; client does not adopt metadata websocket_path automatically or track pong deadline; no Android/WebGL transport acceptance; in-memory state; test dependency websockets has no standalone requirements file; AI/snapshot performance not profiled.
- Formal main repo remains README-only, 0 KB, pull=true/push=false. Legacy repo has only a 3-byte source-like stub. Test mirror remains documentation-only.
- Word audit: FrontlineProtocol_v11.0.0.1_Source_Audit_2026-11-23.docx, 40,174 bytes, SHA-256 4886683afaf09d6828bfefa7f58e966742b3445257d445ad1f16767e2993b617.
- Word update log: FrontlineProtocol_v11.0.0.1_Maintenance_Update_Log_2026-11-23.docx, 37,893 bytes, SHA-256 827928ca4fd35799f8ae0ada240bc443b910af64abf13b2fa25ba73ddb22e9ae.
- Evidence ZIP: FrontlineProtocol_Maintenance_Evidence_2026-11-23.zip, 81,506 bytes, 10 entries, CRC PASS, SHA-256 92275ee87e39640ceccd08ab3bd830ded6d5a76819a9950450dd93022e129f04.
- v12 remains BLOCKED: no full v12 source tree, 12-group art overlay, FieldOperationsCatalog_v12.json or manifests.


## Post-commit verification
- After this documentation-only update, the test mirror has 16 text/documentation files in its recursive main tree and still has no Client/Server/Admin source tree. No binary package was committed.


## 2026-11-23 follow-up execution — run 9
- Current accessible complete archive is the 2026-11-20 v11.0.0.0 package: 1,517,723 bytes, 497 entries, CRC PASS, SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`.
- This run could not retrieve the v11.0.0.1 candidate binary referenced in the prior source-audit entry from the current conversation file listing, recent Library listing or working container. Its rebase against the 2026-11-20 archive remains unverified; formal version stays v11.0.0.0.
- Regression: 12 self-contained + 4 isolated-server entries = 16/16 individually PASS; admin cookie probes 3/3 PASS. Aggregate runner printed ALL PASS but the outer command timed out after the summary without a final exit code.
- Static: integration 495/495; SHA256SUMS 496/496; JSON 57/57; Python 18/18; Unity .meta 145/145 unique GUIDs; 125 asset pairs; OBJ 28 / 1,320 vertices / 928 faces / 0 invalid indices; C# lexical scan 48 files (not compilation).
- No code/config/art/API/protocol/Schema changes; bug counts new/fixed/open 0/0/0. No new full project package or runtime network patch generated.
- New Word report: 40,206 bytes, SHA-256 `fe2bf71bf0ccd63bd287bb31b7d2e4eff6cf88112c8795c9c0028d5fbed2d8e1`.
- New no-code update log: 38,201 bytes, SHA-256 `da51722a54135ff113d662fe84cb176332acf1b738c8e2d8a50c471c0caeb356`.
- New evidence ZIP: 84,061 bytes, 15 entries, CRC PASS, SHA-256 `5ecbe2beabacdc8ad51b266b5393f3981549a8f38114d13a5ebab84561c44b76`.
- v12.0.0.0 remains blocked by missing complete source, art overlay, catalog and manifests.


## 2026-11-24 verification — run 10
- Latest accessible complete source package remains `FrontlineProtocol_v11.0.0.0_Complete_Maintenance_2026-11-20.zip`: 1,517,723 bytes; 497 entries; CRC PASS; SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`.
- Regression: 12/12 self-contained + 4/4 isolated-server entries passed individually; maintenance repeat 5/5; admin cookie probes 3/3. Aggregate runner INCOMPLETE at 300 seconds.
- Static: integration 495/495; SHA256SUMS 496/496; JSON 57/57; Python 18/18; Unity assets/.meta 145/145 with unique GUIDs; OBJ 28 / 1,320 vertices / 928 faces / zero invalid indices; C# lexical scan 48 files (not compilation).
- Client, Unity bundleVersion, 枢纽 Server, Web Admin Panel and PowerShell setup banner agree on v11.0.0.0; API Schema 1; Realtime Protocol 1.
- The complete archive includes a web AdminPanel only; no separate Android Admin/Gradle project is present.
- FP-CLI-001 remains a conditional compatibility risk: metadata publishes websocket_path, but client bootstrap takes the local ServerConfig path before metadata fetch.
- FP-CLI-002 is reclassified as application-level RTT telemetry only; WebSocket control ping/pong is separately handled, with no demonstrated client liveness failure.
- The v11.0.0.1 candidate referenced in older GitHub notes is not present in the current conversation file list, Library search or working container; rebase against the 2026-11-20 package remains unverified. Formal version stays v11.0.0.0.
- No code/config/art/API/protocol/Schema change; Bug Counter new/fixed/open = 0/0/0.
- v12.0.0.0 remains BLOCKED by missing complete Client/枢纽 Server/Admin source, 12-group art overlay, FieldOperationsCatalog_v12.json and v12 manifests.
- Run 10 Word report: 40,592 bytes, SHA-256 `091716308daf766a41d70fcd48add5285362edab44119b1c85d1d4e8a94ec567`.
- Run 10 no-code update log: 38,316 bytes, SHA-256 `5e74edbac68eeaa1c506ff2797611f73093256cebb7d902f532db2c7e1e6339a`.
- Run 10 evidence ZIP: 15 entries, CRC PASS, SHA-256 `ddcf12d87b6d1de1238edd4fe4cf657ff3f2a42797633fbdc97e53ee33046975`.
- No new complete project ZIP or runtime network patch was created; binary artifacts remain in the ChatGPT file workspace, not this mirror.


## 2026-11-25 daily maintenance follow-up — run 11

- This execution physically found and reverified the 2026-11-20 v11.0.0.0 complete archive in the active working container: 1,517,723 bytes, 497 entries, CRC PASS, SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`. This corrects the prior bi-daily run's environment-specific statement that the archive was not present in that earlier execution.
- The 2026-11-19 runtime network patch is present and its 31 payload files match the complete archive byte-for-byte.
- The v11.0.0.1 candidate remains a documentation-only historical reference in this execution; its binary is absent and cannot be rebased.
- All 16 regression entries passed individually; static manifests and assets passed. FP-CLI-001 was confirmed by a live custom WebSocket path probe and remains open pending candidate provenance reconciliation.
- No source tree was added to this documentation test mirror; formal main repository remains unavailable for push.


## 2026-11-26 source import and verification — Run 12

- The current active workspace contains the 2026-11-20 v11.0.0.0 complete archive: 1,517,723 bytes, 497 entries, CRC PASS, SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`.
- Runtime network patch (2026-11-19): 33 entries, CRC PASS; all 31 payload files match the complete archive byte-for-byte.
- Network regression patch (2026-11-20): 5 entries, CRC PASS; manifest classifies it as test-harness only and `runtime_code_changed=false`.
- Regression: 12/12 self-contained + 4/4 isolated-server entries passed individually; maintenance regression repeated 5/5; Admin Cookie probes 3/3. Aggregate runner was not completed as a single process.
- Static integrity: integration manifest 495/495; SHA256SUMS 496/496; JSON 57/57; Python AST/compileall 18/18; Unity .meta 145/145 and 145 unique GUIDs; OBJ 28 / 1,320 vertices / 928 faces / zero invalid indices; C# lexical scan 48 files (not compilation).
- Client, Unity bundleVersion, 枢纽 Server config, Web Admin banner and PowerShell setup banner agree on v11.0.0.0; API Schema 1; Realtime Protocol 1.
- Admin inventory: Web AdminPanel index/login only; no separate Android Gradle Admin project. Android preflight: EditorBuildSettings.asset missing; training controls remain keyboard/mouse oriented.
- FP-CLI-001 confirmed: custom server path /ws-alt is published and accepts WebSocket, while /ws is rejected; Unity bootstrap does not adopt metadata websocket_path.
- Historical v11.0.0.1 candidate binary is unavailable in the current active workspace and cannot be reconciled with the 2026-11-20 497-entry package. Formal version remains v11.0.0.0; no code change or version increment.
- v12.0.0.0 remains BLOCKED by missing complete Client/枢纽 Server/Admin source, 12-group art overlay, FieldOperationsCatalog_v12.json and v12 manifests.
- Run 12 Word report: 40,428 bytes, SHA-256 `9e703c1d1dff263fe9e2278f7a16573d6184053e2e9f89650bc22b78b40d9dc9`.
- Run 12 no-code update log: 38,169 bytes, SHA-256 `5bfcf6ddcf0007f9ad92cd113378ea3fd67786589b3eccf39ad5d0ec79f2ebaf`.
- Run 12 evidence ZIP: 83,589 bytes, 12 entries, CRC PASS, SHA-256 `dc4e6df43b511160f985a96f19ae12d27fbc41696c94705e2b32dcb014e1b936`.
- No source tree or binary artifact was uploaded to this documentation mirror.


## 2026-11-27 source import and verification — Run 13
- Formal release remains v11.0.0.0; the next major milestone target is v12.0.0.0 but release remains blocked.
- The 2026-11-20 complete archive recorded by Run 12 (497 entries; SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`) was not present in the active workspace used by Run 13. The 2026-11-23 v11.0.0.1 candidate binary was also not present. No rebase or promotion was performed.
- The physically accessible 2026-11-15 v11.0.0.0 archive was rechecked: 1,432,078 bytes, 490 entries, CRC PASS, SHA-256 `a2c1e21c12e9076c96394228dfa18be07b8c9a7260183b6bda995933aa1198c9`.
- Runtime network patch: 132,041 bytes, 33 entries, CRC PASS, SHA-256 `0e9478cc73271e5b51106111c2b8b15347d63557bcf474224ed30331a29088d5`; all 33 files match the accessible complete package byte-for-byte.
- Static: integration 488/488; SHA256SUMS 489/489; JSON 56/56; Python compileall 18 files; Unity .meta 145/145 and 145 unique GUIDs; OBJ 28 / 1,320 vertices / 928 faces / zero invalid indices.
- Regression: 12/12 self-contained and 4/4 isolated-server entries PASS individually. Aggregate runner INCOMPLETE at 300 seconds.
- FP-CLI-001 remains confirmed/open: /api/meta advertises websocket_path, while Unity bootstrap continues to assign ServerConfig.websocketPath rather than applying the advertised value.
- No source/runtime/config/art/API/protocol/Schema change, no version increment and no new project or runtime network patch package.
- Run 13 report: 41,370 bytes; SHA-256 `7d2d718c2d40346b582fc52db950f3d21ecfee063229907548f49bf9816b51b5`.
- Run 13 no-code update log: 39,411 bytes; SHA-256 `98b77a2f07fef0150b8e0a4a2ea254f0820d33e18173cd141c4ac5a127ae7118`.
- Run 13 static audit: 40,685 bytes; SHA-256 `486fd81dfe38fed505be1e04f962345a6686c1391f312e35288c0480831ff0f5`.
- Run 13 evidence ZIP: 177,609 bytes, 20 entries, CRC PASS, internal SHA records 19/19; SHA-256 `93cc4945388dc880c2295028acd0afe9a9a57499056cb22bbc5fcf5fff4469a7`.
- Formal main repository remains push=false; this repository is a documentation-only test mirror. No source tree or binary artifact was uploaded.


## 2026-11-27 daily maintenance — Run 14 correction and verification
- The 2026-11-20 v11.0.0.0 complete archive was physically present in the current conversation/mounted workspace and reverified: 1,517,723 bytes; 497 entries; CRC PASS; SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`.
- This supersedes Run 13's environment-specific observation that the 2026-11-20 binary was not available in that earlier execution; the formal release remains v11.0.0.0.
- Integration manifest 495/495; SHA256SUMS 496/496; JSON 57/57; Python 18/18; Unity .meta 145/145 with unique GUIDs; OBJ 28 with zero invalid indices; C# lexical scan 48/48 (not compilation).
- Regression: 12/12 self-contained + 4/4 isolated-server entries PASS individually; maintenance repeat 5/5; Admin Cookie probes 3/3. Aggregate runner did not terminate after printing its ALL PASS summary; aggregate status INCOMPLETE.
- FP-CLI-001 remains confirmed/open. The v11.0.0.1 candidate binary and v12 complete source/asset overlay/manifests remain unavailable.
- No source/runtime/config/art/API/protocol/Schema change; no new complete project ZIP or runtime network patch generated.


## 2026-11-27 periodic source audit — Run 15
- GitHub formal main `We-MCS/Project_Frontline-Protocol`: README-only (28 bytes), tree 1 entry, size 0 KB, push=false.
- Legacy `We-MCS/Frontline-Protocol`: tree 4 entries; only source-like file is a 3-byte FrontlineAndroidBuild.cs; push=false.
- Test mirror `bingjx2013-lang/FrontlineProtocol`: tree 24 documentation/text entries; no Client/Server/Admin source tree; push=true.
- Current Run15 workspace physically contains the historical v11.0.0.1 candidate complete archive (508 entries; CRC PASS; SHA-256 `c918f99eb4370cc0814bea415a88761907597303d01b7b937a554c30444a243d`) and its 30-entry candidate patch (CRC PASS; SHA-256 `995e06544b226c842b738653dc0354d2674d3b9ec7910060689342dfa432f499`).
- The 2026-11-20 v11.0.0.0 497-entry package was verified in Run14 (SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`) but is not accessible in this Run15 file list/mounted workspace. The candidate is based on the 2026-11-15 490-entry baseline; rebase status cannot be confirmed.
- Regression: 12 self-contained + 5 isolated-server entries = 17/17 individually PASS. Aggregate runner TIMEOUT/INCOMPLETE at 300 seconds.
- Static: Python compileall 19/19; JSON 61/61; Integration 506/506; SHA256SUMS 507/507; Unity .meta 145/145 unique; OBJ 28 with zero invalid indices; C# lexical scan 48/48 (not compilation); API paths 11/11; Admin Cookie probes 3/3.
- FP-CLI-001 custom path reproduced: /api/meta advertises /ws-alt, authenticated /ws-alt returns welcome, /ws returns 404, Unity bootstrap does not apply metadata path. OPEN; no patch because official 11/20 source unavailable for rebase.
- FP-NET-002 port collision reproduced: occupied configured port makes the Hub process exit with Errno 98; no automatic port fallback/discovery.
- No runtime source change; formal release remains v11.0.0.0; Bug counts 0/0/0; no v11.0.0.2.
- v12.0.0.0 remains BLOCKED by missing complete Client/Hub Server/Admin source, 12-group art overlay, FieldOperationsCatalog_v12.json and manifests.


## 2026-11-28 source import and verification — Run 16
- Formal main repository remains README-only (28 bytes) and push=false; legacy repository has only a 3-byte source-like C# stub and push=false; writable test mirror remains documentation-only.
- Current accessible complete source is the 2026-11-20 v11.0.0.0 archive: 1,517,723 bytes, 497 entries, CRC PASS, SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`.
- 16/16 regression child tests passed individually; maintenance repeat 5/5; Admin Cookie probes 3/3. Aggregate runner printed ALL PASS but no clean exit status was captured.
- Static: integration 495/495; SHA 496/496; JSON 57/57; Python 18/18; Unity meta 145/145 unique GUIDs; OBJ 28 with zero invalid indices; C# lexical scan 48 files (not compilation).
- FP-CLI-001 re-reproduced; FP-NET-002 confirmed on the formal v11 source (occupied port causes OSError 98; no port fallback or client discovery). No source package or runtime patch was created.
- v11.0.0.1 candidate binary remains unavailable for reconciliation. v12.0.0.0 remains BLOCKED by missing complete Client/Hub Server/Admin source, art overlay, catalog and manifests.
