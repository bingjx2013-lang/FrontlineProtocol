# Frontline Protocol — Daily Maintenance Follow-up (2026-11-25, Run 11)

## Result
- Formal release remains **v11.0.0.0** (A=11, B=0, C=0, D=0). No runtime source/config/art/API/protocol/Schema change was made.
- The current working container physically contains and re-verifies the 2026-11-20 complete archive: 1,517,723 bytes, 497 ZIP entries, CRC PASS, SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`.
- This corrects the earlier same-day bi-daily note that said the 2026-11-20 binary was absent in that earlier execution. It is accessible in this daily follow-up execution.
- The historical v11.0.0.1 candidate (508 entries, SHA-256 `c918f99eb4370cc0814bea415a88761907597303d01b7b937a554c30444a243d`) is still not present in the current workspace or Library title search. Its rebase against the 2026-11-20 package remains unverified. Do not promote it or create v11.0.0.2.

## GitHub
- Formal main `We-MCS/Project_Frontline-Protocol`: main tree contains only README.md; size 0 KB; push=false.
- Legacy `We-MCS/Frontline-Protocol`: four tree entries; source-like C# stub is 3 bytes; push=false.
- Writable test mirror `bingjx2013-lang/FrontlineProtocol`: main HEAD `34206460942d3ed778ccc482ff418b39d5417156`; 20 documentation/index entries; no Client/Server/Admin source tree; push=true. This update is documentation-only.

## Regression
- 12/12 self-contained regression entries PASS, each exit code 0.
- 4/4 isolated-server entries PASS, each run against a fresh disposable loopback server and exit code 0.
- Admin Cookie probes 3/3 PASS (local HTTP default, explicit Secure config, X-Forwarded-Proto=https).
- No one-shot aggregate result was obtained in this run; no aggregate PASS claim is made.

## Static integrity
- Integration manifest 495/495 exact matches; SHA256SUMS 496/496.
- JSON 57/57 parsed; Python 18/18 compileall.
- Unity Assets 145 + .meta 145; 145 unique GUIDs; missing/orphan/duplicate = 0.
- OBJ 28 files, 1,320 vertices, 928 faces, invalid indices = 0.
- C# 48/48 passed a string/comment-aware lexical delimiter scan; this is not C# compilation.
- Art inventory: 30 Prefabs, 184 files under Art, 2 scenes.
- Client/Unity bundleVersion/Hub Server/Admin Panel/PowerShell setup metadata agree on v11.0.0.0; API Schema 1; Realtime Protocol 1. Web AdminPanel has index.html and login.html; no separate Android Gradle project is present.

## Network patch verification
- 2026-11-19 runtime patch: 132,194 bytes, 33 entries, CRC PASS, SHA-256 `3b5c4be9e4909fb3756bf62c594bf3d3b0b617c5911a025dd807c1ca86637afc`; all 31 payload files match the complete project byte-for-byte.
- 2026-11-20 network regression patch: 41,530 bytes, 5 entries, CRC PASS, SHA-256 `c4fa943e9a42f86885522aff3a1b33c067c19902454d090cc6200f0ee4a556c3`; test harness only, not a runtime network patch.

## Confirmed open issue
- **FP-CLI-001**: Server `/api/meta` publishes `websocket_path`, but Unity bootstrap initializes `RealtimeClient.WebSocketPath` from local `ServerConfig.websocketPath` before metadata retrieval and never adopts `meta.websocket_path`.
- Live isolated probe: server configured to `/ws-alt`; `/api/meta` returned `/ws-alt`; WebSocket `/ws-alt` returned `welcome`; default `/ws` was rejected. This confirms a real client/server path mismatch.
- Not fixed because the documented v11.0.0.1 candidate binary is missing and cannot be reconciled. Avoid creating a conflicting same-number candidate.

## Remaining blockers and acceptance
- v12.0.0.0 still lacks complete Client/Hub Server/Admin source, 12-group art overlay, `FieldOperationsCatalog_v12.json`, and version/bug/integration/hash manifests.
- Unity Editor import/C# compilation, Play Mode, CI, Android APK/AAB build/install/device, Windows host, production TLS/WSS, pressure and soak tests were not run.
- This run generated a Word daily report, a Word no-code update log and a 14-entry CRC-PASS evidence ZIP. No new complete source package or runtime network patch was generated.
