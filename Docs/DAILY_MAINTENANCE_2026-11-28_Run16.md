# Project: Frontline Protocol — Daily Maintenance
Date: 2026-11-28 (Asia/Shanghai)
Run: 16
Server node: 枢纽

## Result
Read-only verification, regression, asset integrity scan and isolated network repro completed. No runtime source/config/art/API/protocol/Schema file changed. Formal release remains **v11.0.0.0** (A=11, B=0, C=0, D=0).

## GitHub state
- Formal main `We-MCS/Project_Frontline-Protocol`: main contains only `README.md` (28 bytes), repository size 0 KB, push=false.
- Legacy `We-MCS/Frontline-Protocol`: recursive tree has 4 entries; only source-like file is `Client/Assets/Editor/FrontlineAndroidBuild.cs` (3 bytes), push=false.
- Test mirror `bingjx2013-lang/FrontlineProtocol`: 27 entries, documentation-only, no Client/Server/Admin source tree, push=true. This run updates this mirror's documentation only.

## Current verified source
- Formal source: `FrontlineProtocol_v11.0.0.0_Complete_Maintenance_2026-11-20.zip`, 1,517,723 bytes, 497 entries, CRC PASS, SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`.
- Runtime network overlay: 2026-11-19, 33 entries, CRC PASS, SHA-256 `3b5c4be9e4909fb3756bf62c594bf3d3b0b617c5911a025dd807c1ca86637afc`; 31/31 payload files are byte-identical to the v11 package. This is the historical v10.0.0.2 -> v11.0.0.0 release overlay, not an update patch for an already-v11 installation.
- 2026-11-20 five-entry network regression patch is test-harness only, `runtime_code_changed=false`.
- The v11.0.0.1 candidate binary mentioned in Run15 was not available in this run's mounted workspace, conversation file list or Library search. Do not promote or overwrite it.

## Regression and static checks
- 12 self-contained + 4 isolated-server test entry points: **16/16 child tests PASS**.
- `maintenance_regression_test.py` repeated independently: **5/5 PASS**.
- Admin Cookie probes: **3/3 PASS**.
- Aggregate runner emitted `ALL FRONTLINE REGRESSION TESTS PASS`, but a clean runner exit status was not captured; aggregate status remains **INCOMPLETE**.
- Integration manifest 495/495; SHA256SUMS 496/496; JSON 57/57; Python AST 18/18; Unity .meta 145/145 with 145 unique GUIDs; OBJ 28 files / 1,320 vertices / 928 faces / zero invalid indices; C# lexical delimiter scan 48/48 (not compilation).
- Asset inventory: 30 Prefabs, 184 Art files, 2 scenes, 7 materials, 4 animations.
- Client, Unity bundle, 枢纽 Server, Web Admin and PowerShell admin banners agree on v11.0.0.0; API Schema=1, Realtime Protocol=1. Admin inventory is two Web Admin HTML files; no separate Android Admin Gradle project.

## Confirmed findings
- **FP-CLI-001 / P2 / existing OPEN:** server metadata advertises `/ws-alt`; `/ws-alt` accepts WebSocket and `/ws` is rejected, but Unity Bootstrap still assigns `config.websocketPath` and does not consume `meta.websocket_path`.
- **FP-NET-002 / P2 / confirmed on v11.0.0.0:** when the configured TCP port is occupied, the isolated Hub exits with `OSError [Errno 98] Address already in use`. There is no automatic port fallback, actual-port metadata or client discovery. A server-only fallback would strand Client/Admin, so this requires coordinated Hub, API/Schema, Client, Admin, deployment docs and regression changes.
- **QA-AGG-001 / QA infrastructure / OPEN:** aggregate runner prints all-pass summary but no clean exit status is captured; root cause not isolated.

## Version decision
No increment. Formal version remains **v11.0.0.0**. No v11.0.0.2 is created and no v11.0.0.1 candidate is overwritten. v12.0.0.0 remains BLOCKED by missing complete Client/Hub Server/Admin source, 12-group art overlay, `FieldOperationsCatalog_v12.json` and v12 manifests.

## Not executed
Unity Editor import/C# compilation, Play Mode, CI, Android APK/AAB build/install/device operation, Windows Hub host validation, production TLS/WSS, concurrency load and soak tests.

## Deliverables
- Word daily report: `FrontlineProtocol_Daily_Maintenance_Report_2026-11-28_Run16.docx`, 39,718 bytes, SHA-256 `cb783ed9f350832f33dae89164785c7aa8c56f166cf710b017137ba15a8a4820`.
- Word no-code update log: `FrontlineProtocol_v11.0.0.0_No_Code_Change_Update_Log_2026-11-28_Run16.docx`, 38,552 bytes, SHA-256 `75c0fb1868e9dc6a476bcbe2639a4571ee4dab6827d9e9b6e82576e75e3c3c3b`.
- Evidence ZIP: `FrontlineProtocol_Daily_Maintenance_Evidence_2026-11-28_Run16.zip`, 85,569 bytes, 15 entries, CRC PASS, SHA-256 `59fe099ed3cbdb70f1bd054c4e648931c54e7e98e474c2e2498c3e0fbf959ac0`.
- No new complete source package or runtime patch was generated because no runtime source was changed. Binary artifacts remain in the ChatGPT file workspace, not this GitHub mirror.
