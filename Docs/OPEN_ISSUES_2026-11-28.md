# Frontline Protocol — Open Findings Register
Date: 2026-11-28 · Run 16 · Formal baseline v11.0.0.0

| ID | Priority | Status | Component | Evidence | Required coordinated scope |
|---|---|---|---|---|---|
| FP-CLI-001 | P2 | OPEN (existing) | Unity Client / 枢纽 | `/api/meta` advertises `/ws-alt`; that path accepts WebSocket; `/ws` rejects; Bootstrap still uses `config.websocketPath`. | Client metadata validation/application, regression cases, compatibility docs |
| FP-NET-002 | P2 | OPEN (confirmed on v11.0.0.0) | 枢纽 / Client / Admin / API | Occupied configured port causes `OSError 98`; no automatic fallback, actual-port metadata or discovery. | Hub bind strategy, metadata/API Schema, Client discovery/config, Admin diagnostics, deployment docs, regression |
| QA-AGG-001 | QA infrastructure | OPEN | Tests | 16/16 child tests print PASS; aggregate runner prints ALL PASS but clean exit status is not captured. | Isolate process/pipe lifecycle; preserve exit codes; repeat aggregate execution |
| FP-SEC-001 | P1 for public deployment | OPEN risk | 枢纽 / Admin | Local default `admin_cookie_secure=false`; Hub does not terminate TLS; production TLS/WSS untested. | Trusted TLS reverse proxy, Secure cookie, proxy trust validation, WSS acceptance |

## Counting / release note
- FP-CLI-001 is carried forward and is not counted again as a new issue.
- FP-NET-002 was newly confirmed against the accessible formal v11.0.0.0 source tree and is recorded in this maintenance ledger. The shipped `BUG_FIX_COUNTER_v11.0.0.0.json` was not edited in place because no formal source release was made; reconcile it in the next coordinated release package.
- QA-AGG-001 is test infrastructure, not a runtime gameplay bug.
- No source, config, art, API, protocol or Schema files were changed.
