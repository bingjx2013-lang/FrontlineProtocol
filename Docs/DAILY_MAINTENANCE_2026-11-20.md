# Daily Maintenance — 2026-11-20

Project: Frontline Protocol《前线协议》

## Verified baseline
- Latest accessible complete project package: **v11.0.0.0**, maintenance refresh dated 2026-11-20.
- v12.0.0.0 remains a handover target only; the complete v12 source and art overlay are unavailable.

## GitHub audit
- Formal main repository: We-MCS/Project_Frontline-Protocol, main contains only README.md, 0 KB, pull=true / push=false.
- Old repository: We-MCS/Frontline-Protocol, 2 KB, latest commit 00abd9dee7dab543a158ffbdb0831685661a6fdc on 2026-10-30; not the formal main.
- User-owned test mirror: bingjx2013-lang/FrontlineProtocol, main, 44 KB, pull/push/admin true, text-only. Latest commit before this maintenance: 84e7d5991f43542c4bd6b26e77cb64ed0ce2ffae.
- No binary source archive was uploaded to GitHub.

## Regression and static checks
- 16/16 regression entry points passed individually (12 self-contained + 4 isolated-server).
- Corrected maintenance regression passed five additional consecutive runs.
- The aggregate runner exceeded the 300-second command window; it is not marked as passed.
- Python compileall: 18 files; JSON: 57/57; INTEGRATION_MANIFEST: 495/495; SHA256SUMS: 496/496.
- Unity .meta: 145/145 paired, 145 unique GUIDs.
- OBJ: 28 files, 1,320 vertices, 928 faces, zero invalid indices.
- C# delimiter scan: 48 files; not a C# compile.

## Change made
- Fixed TEST-WS-001 in Tests/maintenance_regression_test.py. The test now ignores periodic snapshot frames while waiting for the expected WebSocket event, with a five-second deadline.
- Runtime server/client code, config, art, API, protocol and Schema unchanged.
- Runtime bug counts new/fixed/open: 0/0/0. Formal version remains v11.0.0.0.

## Not run / blocked
- Unity Editor import/compile, Play Mode, CI, APK/AAB, Android device, Windows host, production TLS/WSS, pressure and soak tests were not run.
- v12 complete Client, Hub Server (枢纽), Admin/AdminPanel, 12-group art overlay, FieldOperationsCatalog_v12.json and v12 manifests remain unavailable.
