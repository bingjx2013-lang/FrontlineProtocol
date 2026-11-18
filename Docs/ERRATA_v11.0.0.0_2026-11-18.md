# v11.0.0.0 Documentation Errata — Reconciled 2026-11-19

Status: documentation/metadata maintenance record. Formal version remains v11.0.0.0.

## Prior ERR-DOC-001 — WebSocket token statement (WITHDRAWN)

The 2026-11-18 note classified a sentence in Server/README.md as stale. Reinspection shows that sentence is inside the **v6.0.3.1 historical maintenance record**, not the current protocol contract. The current protocol section later in the same README requires Authorization: Bearer <token> and rejects query-string tokens; the server implementation and regression tests agree. The prior classification was incorrect and is withdrawn. Historical release history is left intact.

## DOC-003 — JSON inventory count (CORRECTED)

The archive contains 56 JSON files, and all 56 parse successfully. Updated:
- VALIDATION_REPORT_v11.0.0.0.json
- MAINTENANCE_STATUS_v11.0.0.0.json
- TEST_RUN_REPORT_v11.0.0.0.txt
- MILESTONE_REPORT_v11.0.0.0.md

All counts now state 56.

## DOC-004 — Network patch payload count (CORRECTED)

The network patch contains 31 payload files plus PATCH_MANIFEST_v11.0.0.0.json and PATCH_SHA256SUMS_v11.0.0.0.txt, totaling 33 ZIP entries. Updated the validation and maintenance status counts from 30 to 31. Rebuilt patch and integration manifests/checksum files.

## Bug counter and release boundary

metadata_hygiene_corrections increased from 1 to 3. Runtime bugs newly registered/fixed/open remain 0. No runtime source, configuration, art, API, protocol or Schema changed. No formal version increment was made.

## Deployment note

admin_cookie_secure=false remains the documented local HTTP default. Production TLS/reverse-proxy deployment must enable Secure Cookie or use the trusted HTTPS forwarding arrangement documented in Server/ADMIN_SECRET_SETUP.md.
