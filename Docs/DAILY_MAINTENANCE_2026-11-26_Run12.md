# Frontline Protocol — Daily Maintenance 2026-11-26 (Run 12)

## Result
- Formal version remains **v11.0.0.0**. No runtime source/config/art/API/protocol/Schema change was made.
- Current active workspace contains and re-verifies the 2026-11-20 v11.0.0.0 complete archive: 1,517,723 bytes, 497 entries, CRC PASS, SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`.
- The current conversation file listing includes the 2026-11-20 complete package and 11/19 runtime patch, but not the 11/25 Run 11 Word/evidence binaries referenced in the prior GitHub record. This run regenerates the daily report, no-code update log and evidence ZIP.

## GitHub
- `We-MCS/Project_Frontline-Protocol`: main contains only README.md; size 0 KB; push=false.
- `We-MCS/Frontline-Protocol`: legacy repo, four tree entries; push=false; not a complete source tree.
- `bingjx2013-lang/FrontlineProtocol`: writable documentation mirror; main tree had 21 entries before this run, no Client/Server/Admin source tree. Only documentation/index records are maintained here; no binary source package is committed.

## Regression
- 12/12 self-contained and 4/4 isolated-server entry points passed individually.
- Maintenance regression repeated 5/5.
- Admin Cookie probes 3/3.
- Aggregate runner was not completed as a single process; do not label it PASS.
- FP-CLI-001 custom path probe reproduced the mismatch: `/api/meta` advertises `/ws-alt`, `/ws-alt` accepts a WebSocket, `/ws` is rejected; bootstrap does not apply `meta.websocket_path`.

## Static integrity
- ZIP 497 entries CRC PASS; integration manifest 495/495; SHA256SUMS 496/496.
- JSON 57/57; Python 18/18 AST and compileall; Unity .meta 145/145, 145 unique GUIDs; OBJ 28, 1,320 vertices, 928 faces, zero invalid indices; C# 48-file lexical delimiter scan PASS (not compilation).
- Art inventory: 30 Prefabs, 184 Art files, 2 scenes.
- Client, Unity bundleVersion, 枢纽 config, Web Admin banner and PowerShell setup banner agree on v11.0.0.0; API Schema 1; Realtime Protocol 1.
- Admin is Web AdminPanel only; no separate Android Gradle admin project. Android preflight remains blocked by missing EditorBuildSettings and mobile input/build configuration.

## Issue and blockers
- FP-CLI-001 remains confirmed/open. No code change was made because the historical v11.0.0.1 candidate binary is unavailable and cannot be reconciled against the current 2026-11-20 package. Do not create a different artifact under the same candidate version; do not create v11.0.0.2 without resolving the provenance conflict.
- v12.0.0.0 remains BLOCKED: complete Client/Hub Server/Admin source, 12-group art overlay, `FieldOperationsCatalog_v12.json`, and v12 version/bug/integration/hash manifests are not accessible.
- Unity Editor import/C# compilation, Play Mode, CI, APK/AAB build/install, Windows host, production TLS/WSS, pressure and soak were not run.

## Deliverables
- Word daily maintenance report: 40,428 bytes; SHA-256 `9e703c1d1dff263fe9e2278f7a16573d6184053e2e9f89650bc22b78b40d9dc9`.
- Word no-code update log: 38,169 bytes; SHA-256 `5bfcf6ddcf0007f9ad92cd113378ea3fd67786589b3eccf39ad5d0ec79f2ebaf`.
- Evidence ZIP: 83,589 bytes; 12 entries; CRC PASS; SHA-256 `dc4e6df43b511160f985a96f19ae12d27fbc41696c94705e2b32dcb014e1b936`.
- No new complete source package or runtime network patch was generated. Existing verified 2026-11-20 complete archive and 2026-11-19 runtime patch remain reference artifacts only.
