# Daily Maintenance — 2026-11-21

Project: Frontline Protocol《前线协议》

## Verified baseline
- Latest accessible complete source package remains **v11.0.0.0**, maintenance refresh dated 2026-11-20.
- Complete package: `FrontlineProtocol_v11.0.0.0_Complete_Maintenance_2026-11-20.zip`, 1,517,723 bytes, 497 ZIP entries, CRC PASS, SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`.
- v12.0.0.0 remains a handover target only. The complete v12 Client/Hub Server/Admin source tree, 12-group art overlay and v12 manifests are not accessible.

## GitHub audit
- Formal main repository: We-MCS/Project_Frontline-Protocol; main contains only README.md (28 bytes), repository size 0 KB, current connector permission pull=true / push=false.
- Old repository: We-MCS/Frontline-Protocol; latest commit `00abd9dee7dab543a158ffbdb0831685661a6fdc` dated 2026-10-30. Recursive tree contains only `Assets/Editor/FrontlineAndroidBuild.cs` (3 bytes) and directories.
- User-owned test mirror: bingjx2013-lang/FrontlineProtocol; main, 53 KB before this documentation update, push permission available, text-only. Latest commit before this maintenance: `f5161f9322858247113d7acd3a4576432930697e`.
- No source archive, binary package or APK was committed to GitHub in this run.

## Regression
- 16/16 entry points passed individually: 12 self-contained + 4 isolated-server tests.
- `maintenance_regression_test.py` passed five additional consecutive runs (5/5).
- Aggregate `Tests/run_regression_suite.py` did not complete within the 300-second execution window and emitted no final summary. It is recorded INCOMPLETE, not PASS. The individual test entries were executed separately, including HTTP smoke and v11 metadata compatibility.

## Static and asset integrity
- Complete ZIP: 497 entries; CRC PASS.
- 2026-11-20 network regression test patch: 5 entries; CRC PASS. Its sole payload `Tests/maintenance_regression_test.py` is byte-identical to the full project copy. It is a test-harness patch, not a runtime network patch.
- INTEGRATION_MANIFEST: 495/495 files exist with exact size and SHA-256.
- SHA256SUMS: 496/496 records match.
- JSON: 57 total files parse; 56 project JSON files excluding the self-referential integration manifest, plus the manifest itself.
- Python: 18 files; `compileall` exit code 0.
- Unity `.meta`: 145/145 asset pairs; 145 unique GUIDs; missing/orphan/duplicate = 0.
- OBJ: 28 files, 1,320 vertices, 928 faces, invalid face indices = 0.
- C#: 48 files passed lexical delimiter/structure scan; this is not a C# compiler.
- Version markers synchronized: Client VERSION, Unity bundleVersion, Hub config, Admin Panel banner, PowerShell setup banner and VERSION.md all v11.0.0.0; Hub node name is 枢纽.

## Module review
- Client/gameplay regression coverage passed for room readiness, room-scoped shooting, movement/spawn bounds, reload/ammo, AI/GOAP source guards and match state. No runtime code change was made.
- Art static checks passed for v11 assets; Unity rendering/UV/PBR/LOD/rig/collider acceptance remains external.
- Hub Server HTTP/WebSocket/API metadata/auth tests passed in isolated processes.
- `Server/AdminPanel` is present. No separate Android Admin app exists in the verified v11 archive.
- API Schema v1 and Realtime Protocol v1 remain unchanged.

## Issues and actions
- `TEST-AGG-001` (test tooling observation): aggregate suite does not complete within 300 seconds in this environment. Individual tests pass. No runner code was changed because the cause is not yet isolated to a reproducible source defect. This is not a runtime Bug Counter item.
- Production reminder: `admin_cookie_secure=false` is the documented local HTTP default. Production TLS/reverse-proxy deployment must enable Secure Cookie or use the documented trusted HTTPS forwarding signal. No production environment was available to validate.
- No new runtime bugs registered, fixed or left open: 0/0/0. Metadata hygiene corrections remain 3.

## Version decision and change boundary
- Formal version remains **v11.0.0.0** (A=11, B=0, C=0, D=0).
- No source/config/API/protocol/Schema/art changes this run; no new complete project package or runtime network patch was created.
- The 2026-11-20 complete package and test-only patch remain the latest actual deliverables. The 2026-11-19 network/runtime patch remains the latest runtime network patch.

## Not run / blocked
- Unity Editor import/compile, Play Mode, CI, APK/AAB, Android install/device, Windows host service, production TLS/WSS, load/pressure and soak tests were not run.
- v12 complete Client, Hub Server (枢纽), Admin/AdminPanel, 12-group art overlay, `FieldOperationsCatalog_v12.json`, VERSION, BUG_FIX_COUNTER, BUG_REGISTER, INTEGRATION_MANIFEST and SHA256SUMS remain unavailable.
