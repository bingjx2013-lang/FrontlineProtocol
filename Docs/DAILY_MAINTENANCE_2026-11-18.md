# Daily Maintenance — 2026-11-18

Project: Frontline Protocol《前线协议》

Verified complete source baseline: **v11.0.0.0**. Handover target **v12.0.0.0 remains BLOCKED**, not a verified source baseline.

## GitHub and source inventory

- Formal main repository `We-MCS/Project_Frontline-Protocol`, branch `main`: 0 KB, only README is retrievable; latest commit `d5fd155bdb482125b98d169a9a81d458de0c9180` (Initial commit, 2026-11-15T00:10:18Z); current permission pull=true / push=false. Code searches for `FrontlineClientBootstrap`, `API_SCHEMA_v1`, and `VERSION.md` returned no source hits.
- Test mirror `bingjx2013-lang/FrontlineProtocol`, branch `main`: 26 KB before this documentation update; push permission true. It is a user-owned test mirror, not the formal main repository.
- v11 complete ZIP: 1,432,078 bytes; 490 entries; CRC PASS; SHA-256 `a2c1e21c12e9076c96394228dfa18be07b8c9a7260183b6bda995933aa1198c9`.
- v11 network patch: 132,041 bytes; 33 entries; CRC PASS; SHA-256 `0e9478cc73271e5b51106111c2b8b15347d63557bcf474224ed30331a29088d5`; all 33 files are byte-identical to corresponding files in the complete archive.

## Regression

- 12 self-contained regression entries: 12/12 PASS individually.
- 4 isolated-server entries: 4/4 PASS individually.
- Aggregate `Tests/run_regression_suite.py` exceeded the 300-second command window; recorded as TIMEOUT, not PASS.

## Static and asset integrity

- Integration manifest: 488/488 files present with exact size and SHA-256.
- SHA256SUMS: 489/489 records match.
- JSON: 56/56 parse; two v11 validation/status JSON documents still report 54.
- Python: 18 files; compileall PASS.
- Unity assets: 145/145 `.meta` pairs, 145 unique GUIDs, no missing/orphan metadata.
- OBJ: 28 files, 1,320 vertices, 928 faces, zero invalid indices.
- C#: 48 files pass delimiter-structure scan only; this is not C# compilation.
- Version metadata: Client VERSION, Unity bundleVersion and Hub Server config all say v11.0.0.0; API Schema 1 / Realtime Protocol 1; node name 枢纽.

## Findings and corrective record

1. `Server/README.md` contains a stale line claiming WebSocket query-string token authentication; current v11 tests confirm Bearer-header authentication and query-token rejection. Recorded in `Docs/ERRATA_v11.0.0.0_2026-11-18.md`.
2. JSON count discrepancy 54 vs 56; all 56 parse. Recorded in the same errata.
3. `admin_cookie_secure=false` is the documented local HTTP default; production TLS deployment requirements remain documented.
4. AdminPanel is a Web console; no separate Android Admin project was found in this package.

## Changes and release decision

No source code, configuration, art, API, protocol or Schema files were changed. Only documentation errata and this maintenance record were prepared for the user-owned test mirror. Formal version remains **v11.0.0.0**; no new complete project ZIP or network patch was generated.

## Not executed / blocked

Unity Editor import/compile, Play Mode, CI, APK/AAB build, Android install/device test, Windows host acceptance, production TLS/WSS, pressure/soak tests were not executed. v12 Client/Hub Server/Admin source, 12-group art overlay, `FieldOperationsCatalog_v12.json` and v12 version/bug/integration manifests remain unavailable.
