# v11.0.0.0 Documentation Errata — 2026-11-18

Status: corrective maintenance note only; the published v11.0.0.0 ZIP remains immutable.

## ERR-DOC-001 — WebSocket token transport statement

`Server/README.md` contains an older statement that the WebSocket handshake still uses a query-string token. The current v11.0.0.0 server/client contract and the passing `deep_source_hardening_regression_test.py` establish that the WebSocket handshake uses `Authorization: Bearer <token>` and query-string tokens are rejected.

Recommended replacement:

> HTTP API and WebSocket handshake authenticate client sessions through the `Authorization: Bearer` header. Query-string tokens are rejected.

The original v11 archive was not modified; this correction is recorded for the next formal source package.

## ERR-DOC-002 — JSON file count

`VALIDATION_REPORT_v11.0.0.0.json` and `MAINTENANCE_STATUS_v11.0.0.0.json` state 54 JSON files. A fresh recursive scan of the 490-entry archive found 56 JSON files; all 56 parse successfully.

Update both counts to 56 in the next formal package and regenerate affected manifests/checksums if the files are changed.

## Deployment note — Secure Cookie

`admin_cookie_secure=false` is the documented local HTTP development default. Production TLS/reverse-proxy deployment must enable Secure Cookie or pass the trusted HTTPS forwarding signal as described by `Server/ADMIN_SECRET_SETUP.md`. This is not classified as a runtime defect in the current local configuration.

## Release boundary

No code, API, protocol, Schema, configuration, or art asset was modified in this maintenance run. No four-segment version increment was made. This errata is a documentation record, not a v11.0.0.1 release and not a replacement source archive.
