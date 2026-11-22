# Frontline Protocol Daily Maintenance — 2026-11-23

## Result

This run rechecked the accessible v11.0.0.1 candidate package, all three known GitHub repositories, source integrity, regression tests, network/authentication paths and unresolved release provenance. No new runtime defect was proven that could be safely changed and fully validated in this environment. No runtime source code was changed and no new formal version was created.

## Repository access

- Formal main repository `We-MCS/Project_Frontline-Protocol`: main contains only a 28-byte README; repository size 0 KB; connector permissions `pull=true / push=false`.
- Legacy repository `We-MCS/Frontline-Protocol`: recursive tree has four entries; the only source-like file is a 3-byte `Client/Assets/Editor/FrontlineAndroidBuild.cs`; `push=false`.
- Test mirror `bingjx2013-lang/FrontlineProtocol`: 15 text/documentation files only, no Client/Server/Admin source tree; `push=true`. Latest recorded commit is `d39ff701f2fe97df312cf1cbe6a5f1446d8c1144` (2026-11-21T19:02:01Z).

## Accessible candidate package

- `FrontlineProtocol_v11.0.0.1_Complete.zip`: 1,576,260 bytes; 508 entries; CRC PASS; SHA-256 `c918f99eb4370cc0814bea415a88761907597303d01b7b937a554c30444a243d`.
- `FrontlineProtocol_v11.0.0.1_Network_And_Runtime_Patch.zip`: 133,688 bytes; 30 entries; CRC PASS; SHA-256 `995e06544b226c842b738653dc0354d2674d3b9ec7910060689342dfa432f499`.
- Scope: 48 C# files, 19 Python files, 2 AdminPanel HTML files, 145/145 Unity .meta pairs, 145 unique GUIDs, 28 OBJ files. Admin is Web AdminPanel only; no separate Android Admin source was found.

## Verification

- Regression suite: 17/17 entries PASS; final summary `ALL FRONTLINE REGRESSION TESTS PASS`.
- Python compileall and AST: 19/19 PASS.
- JSON: 61/61 PASS.
- Integration manifest: 506/506 exact.
- SHA256SUMS: 507/507 exact.
- Unity .meta: 145/145 pairs; 145 unique GUIDs.
- OBJ: 28 files; 1,320 vertices; 928 faces; zero invalid indices.
- C#: 48-file lexical delimiter scan PASS (not C# compilation).
- Client/server API literal path parity: 11/11.
- Admin cookie probes: 3/3 PASS (local HTTP default; explicit Secure config; X-Forwarded-Proto=https).

## Risk register

- **P1 FP-REL-001 — release provenance conflict:** run 8 records the formal release as v11.0.0.0 and points to a 2026-11-20 497-entry package (SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`), but that binary is not accessible in the current file workspace/Library. The available v11.0.0.1 package is based on the 2026-11-15 490-entry v11.0.0.0 baseline. Rebase status against the 11/20 refresh cannot be confirmed.
- **P1 FP-SEC-001 — public deployment:** `admin_cookie_secure=false` is the local HTTP default. Production must terminate TLS at a trusted reverse proxy and enable Secure cookies; production TLS/WSS was not tested.
- **P2 FP-NET-002 — ports/discovery:** 枢纽 binds configured host/port, default `0.0.0.0:8080`; no automatic port fallback or node discovery. A busy port prevents startup.
- **P2 FP-CLI-001 — WebSocket path negotiation:** the server advertises `websocket_path` in `/api/meta`, but the Unity client still uses `ServerConfig.websocketPath`; non-default paths need manual synchronization.
- **P2 FP-CLI-002 — client liveness:** client sends application pings but does not track pong timestamps or enforce a client-side pong deadline.
- **P2 FP-PLAT-001 — platform:** WebGL transport is not implemented; Android build/install was not executed; no Android Admin source exists in the archive.
- **P2 FP-DATA-001 — persistence:** player/session/room state is in-memory and the node has a two-hour lifetime.
- **P2 FP-QA-001 — test reproducibility:** tests import `websockets`, but no standalone test requirements file is present.
- **P3 FP-PERF-001/002 — performance:** AI perception/cover scans allocate and scan scene objects; snapshot serialization/broadcast has not been profiled or load-tested.

## Version decision

Runtime bugs newly registered/fixed/open in this run: **0/0/0**. No version increment is justified. Keep the accessible v11.0.0.1 archive labelled as a verified candidate, but do not promote it to the official latest baseline until the missing 2026-11-20 package is restored and compared. Do not create v11.0.0.2.

v12.0.0.0 remains BLOCKED: complete Client/枢纽/Admin source, 12-group art overlay, `FieldOperationsCatalog_v12.json` and v12 manifests are not accessible.

## Not executed

Unity Editor import/C# compilation, Play Mode, CI, APK/AAB build, Android installation, Windows batch runtime validation, production TLS/WSS, concurrency load and soak tests.

## Delivery records

- Word audit: `FrontlineProtocol_v11.0.0.1_Source_Audit_2026-11-23.docx` — 40,174 bytes; SHA-256 `4886683afaf09d6828bfefa7f58e966742b3445257d445ad1f16767e2993b617`.
- Word update log: `FrontlineProtocol_v11.0.0.1_Maintenance_Update_Log_2026-11-23.docx` — 37,893 bytes; SHA-256 `827928ca4fd35799f8ae0ada240bc443b910af64abf13b2fa25ba73ddb22e9ae`.
- Evidence ZIP: `FrontlineProtocol_Maintenance_Evidence_2026-11-23.zip` — 81,506 bytes; 10 entries; CRC PASS; SHA-256 `92275ee87e39640ceccd08ab3bd830ded6d5a76819a9950450dd93022e129f04`.

The binary source and patch archives remain in the ChatGPT file workspace and are not committed to GitHub. This test-mirror update is documentation-only.


## Post-commit verification
- After this documentation-only update, the test mirror has 16 text/documentation files in its recursive main tree and still has no Client/Server/Admin source tree. No binary package was committed.
