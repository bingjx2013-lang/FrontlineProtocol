# Source Audit — Run 15 / 2026-11-27

## Scope
Accessible candidate archive: `FrontlineProtocol_v11.0.0.1_Complete.zip`, 508 entries, CRC PASS, SHA-256 `c918f99eb4370cc0814bea415a88761907597303d01b7b937a554c30444a243d`.
Static inventory: 19 Python files, 48 C# files, 2 Web AdminPanel HTML files, 145 Unity .meta pairs, 28 OBJ files. The current GitHub repositories do not contain a complete source tree.

Manual focus review covered the Hub HTTP/WebSocket/auth/session/room paths, Unity bootstrap/API models/ServerConfig/Auth/Realtime client, AI perception/tactical planning/GOAP, AdminPanel rendering and CSRF, and associated regression scripts. All listed source files also received the static/integrity checks recorded in the daily report. This is not a claim of Unity compilation or full runtime acceptance.

## Reproduced issues
### FP-CLI-001 — P2 — OPEN
Custom WebSocket path mismatch. Isolated Hub configured with `websocket_path=/ws-alt` publishes `/ws-alt` in `/api/meta`; authenticated `/ws-alt` receives `welcome`; `/ws` returns 404. `ServerMetaResponse` includes the field, but `FrontlineClientBootstrap` does not apply it and continues to use `ServerConfig.websocketPath`.
Proposed correction: validate metadata as a safe origin-relative path after protocol compatibility succeeds, apply it to `RealtimeClient.WebSocketPath`, and retain configured fallback when metadata is unavailable. Reject absolute URLs, query/fragment, CR/LF, backslashes and traversal segments.
Not patched in this run because the latest official 2026-11-20 source tree is unavailable for rebase.

### FP-NET-002 — P2 — OPEN
The Hub binds the configured fixed port. A live isolated port-conflict probe returned `OSError: [Errno 98] Address already in use`; no automatic fallback or discovery exists. Any implementation must synchronize server bind selection, /api/meta and /health endpoint data, client discovery/reconnect, Admin display and deployment/firewall docs.

## Risk register
| ID | Level | Evidence | State |
|---|---|---|---|
| FP-REL-001 | P1 | 11/20 official 497-entry source archive not available in this run; v11.0.0.1 candidate derives from 11/15 baseline | BLOCKED |
| FP-REPO-001 | P1 | Formal main is README-only and push=false; test mirror has no source tree | BLOCKED |
| FP-SEC-001 | P1* | HTTP default, admin_cookie_secure=false; TLS/WSS production acceptance absent | Not fixed; production-only P1 |
| FP-CLI-001 | P2 | Custom /ws-alt mismatch reproduced | OPEN |
| FP-NET-002 | P2 | Fixed port collision reproduced | OPEN |
| FP-DATA-001 | P2 | Session/player/room state is in-memory | Known prototype limitation |
| FP-PLAT-001 | P2 | WebGL transport disabled; build scene list absent; touch controls absent | Not accepted |
| FP-PERF-001 | P3 | Perception allocations and full cover scan per plan | Needs Unity Profiler |
| FP-PERF-002 | P3 | No concurrency/soak data | Unquantified |

## Test results
17/17 regression entry points passed individually (12 self-contained + 5 isolated-server). Aggregate runner timed out at 300 seconds and is recorded INCOMPLETE. Python compileall 19/19, JSON 61/61, Integration Manifest 506/506, SHA256SUMS 507/507, .meta 145/145, OBJ 28/28, C# lexical scan 48/48 (not compile), API path literals 11/11, Admin Cookie probes 3/3.

## Version
Formal release remains v11.0.0.0, A=11/B=0/C=0/D=0. Runtime bug counts for this run: 0/0/0. No v11.0.0.2 created. v11.0.0.1 remains an unreconciled historical candidate.
