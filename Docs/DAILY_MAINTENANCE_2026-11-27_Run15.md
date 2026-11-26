# Frontline Protocol — Daily Maintenance / Source Audit
Date: 2026-11-27 (Asia/Shanghai)
Run: 15
Server node: 枢纽

## Result
Read-only audit and verification completed. No runtime source change was made and no release version was incremented. Formal release remains **v11.0.0.0** (A=11, B=0, C=0, D=0). Runtime Bug counts for this run: newly registered 0 / fixed 0 / newly opened 0.

## GitHub repositories
- Formal main `We-MCS/Project_Frontline-Protocol`: main tree contains only README.md (28 bytes), repository size 0 KB, push=false.
- Legacy `We-MCS/Frontline-Protocol`: 4 tree entries; only source-like file is a 3-byte FrontlineAndroidBuild.cs; push=false.
- Test mirror `bingjx2013-lang/FrontlineProtocol`: 24 text/documentation entries; no Client/Server/Admin source tree; push=true.
- This commit updates documentation in the test mirror only. No project source or binary archive was uploaded.

## Accessible source scope
The current run can physically access the historical candidate `FrontlineProtocol_v11.0.0.1_Complete.zip` (1,576,260 bytes; 508 entries; CRC PASS; SHA-256 `c918f99eb4370cc0814bea415a88761907597303d01b7b937a554c30444a243d`).
- Server: 2 Python files; server.py 1,862 lines.
- Tests: 17 Python files; 2,365 lines.
- Unity client: 48 C# files; 2,723 lines.
- Admin: 2 Web AdminPanel HTML files; no separate Android Admin project.
- Unity metadata: 145/145 .meta pairs; 145 unique GUIDs.
- OBJ: 28 files; 1,320 vertices; 928 faces; zero invalid indices.

The latest formal source record in VERSION.md is the 2026-11-20 v11.0.0.0 refresh (497 entries; SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`). It was recorded as physically verified in Run14 but is not present in the current Run15 file list or mounted container. The accessible v11.0.0.1 candidate is based on the 2026-11-15 490-entry v11.0.0.0 baseline; its rebase against 11/20 cannot be confirmed. Do not promote it.

## Static checks and regression
- Candidate ZIP: 508 entries; CRC PASS.
- Integration manifest: 506/506 exact size/hash PASS.
- SHA256SUMS: 507/507 PASS.
- JSON: 61/61 PASS.
- Python compileall: 19/19 PASS.
- Regression: 12 self-contained + 5 isolated-server entries = 17/17 individually PASS.
- Aggregate runner: TIMEOUT/INCOMPLETE at 300 seconds; each test entry was then run independently.
- Unity .meta: 145/145 pairs; 145 unique GUIDs; no orphan/missing metadata.
- OBJ: 28 files; 1,320 vertices; 928 faces; zero invalid indices.
- C#: 48-file lexical delimiter scan PASS; not C# compilation.
- Client HTTP API literals: 11/11 present in server route literals.
- Admin Cookie probes: 3/3 PASS (local HTTP default, explicit Secure config, X-Forwarded-Proto=https).

## Reproduced findings
- **FP-CLI-001 / P2:** With server websocket_path=/ws-alt, /api/meta advertises /ws-alt; authenticated /ws-alt returns welcome; /ws returns 404. The DTO contains websocket_path, but Unity bootstrap still uses config.websocketPath and does not consume meta.websocket_path. OPEN; not patched because the 11/20 formal source tree is unavailable for rebase.
- **FP-NET-002 / P2:** An occupied configured port makes the isolated Hub server exit with OSError Errno 98 Address already in use. No automatic port fallback or client discovery exists.

## Other risks
- **FP-SEC-001 / P1 for public deployment:** admin_cookie_secure=false is the local HTTP default; the Hub does not terminate TLS. Production TLS/WSS was not tested.
- **FP-DATA-001 / P2:** sessions, players and rooms are in-memory only; default process lifetime is 7200 seconds.
- **FP-PLAT-001 / P2:** WebGL ClientWebSocket transport is disabled; EditorBuildSettings.asset is absent; training controls are keyboard/mouse oriented.
- **FP-PERF-001 / P3:** AI perception allocates OverlapSphere results and collections; tactical cover search calls FindObjectsOfType per plan.
- **FP-PERF-002 / P3:** no concurrency load or long-duration soak evidence.

## Version decision
No increment. Formal v11.0.0.0 remains A=11, B=0, C=0, D=0. FP-CLI-001 is already registered OPEN and was not counted again. No v11.0.0.2 was created.

## Not executed
Unity Editor import/C# compile, Play Mode, CI, Android APK/AAB build/install/device operation, Windows host service validation, production TLS/WSS, concurrency load and soak tests.

## Blockers
The 2026-11-20 official source archive, 2026-11-19 runtime patch binary, and complete v12 Client/Hub Server/Admin source plus 12-group art overlay/catalog/manifests were not accessible in this run.
