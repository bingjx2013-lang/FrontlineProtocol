# Frontline Protocol — Daily Maintenance 2026-11-27 (Run 14)

## Result
- Formal release remains **v11.0.0.0**. No runtime source/config/art/API/protocol/Schema change was made.
- Correctly verified the 2026-11-20 complete package physically present in this run: 1,517,723 bytes, 497 entries, CRC PASS, SHA-256 `ed2c4420a2f0616aef295548c4146cb69f5888a6a603536767011b841c3c333e`.
- This corrects the environment-specific Run 13 note that the 2026-11-20 binary was unavailable in that earlier run.
- No new full source package or runtime patch was generated.

## GitHub
- Formal main `We-MCS/Project_Frontline-Protocol`: main tree has one file (`README.md`, 28 bytes), size 0 KB, push=false.
- Legacy `We-MCS/Frontline-Protocol`: four tree entries; only source-like file is a 3-byte C# stub; push=false.
- Writable mirror `bingjx2013-lang/FrontlineProtocol`: 23 tree entries, documentation/index only, no Client/Server/Admin source; push=true.
- `bingjx2013-lang/-SYNC` tree: 12 entries, no Frontline paths.
- Latest mirror commit before Run 14: `75673d060cd02b4e90c298411cfa2e5ecc872eb6` (Run 13 docs).
- Run 13 Word/evidence binaries are listed in its GitHub note but are not present in the current conversation files or mounted workspace.

## Regression
- 12/12 self-contained and 4/4 isolated-server tests passed individually: **16/16**.
- Maintenance regression repeated 5/5.
- Admin Cookie probes 3/3.
- Aggregate runner emitted all PASS lines and an ALL PASS summary but did not exit within the post-summary execution window; aggregate status remains INCOMPLETE.
- FP-CLI-001 reproduced: `/api/meta` advertises `/ws-alt`; `/ws-alt` returns welcome; `/ws` is rejected; Unity bootstrap does not apply `meta.websocket_path`.

## Static integrity
- Integration manifest 495/495; SHA256SUMS 496/496; JSON 57/57; Python 18/18 AST and compileall.
- Unity `.meta` 145/145 with 145 unique GUIDs; OBJ 28 / 1,320 vertices / 928 faces / zero invalid indices; C# 48-file lexical delimiter scan (not compilation).
- Art inventory: 30 Prefabs, 184 Art files, 2 scenes.
- Client, Unity bundleVersion, 枢纽 config, Web Admin banner and PowerShell setup banner agree on v11.0.0.0; API Schema 1; Realtime Protocol 1.
- Web AdminPanel exists; no separate Android Gradle Admin project. Android preflight lacks EditorBuildSettings and mobile build/input settings.

## Issues and blockers
- FP-CLI-001 remains confirmed/open; not fixed because the historical v11.0.0.1 candidate binary is unavailable and cannot be reconciled. No conflicting v11.0.0.1 or skipped v11.0.0.2 artifact was created.
- QA-AGG-001: aggregate test runner process does not exit cleanly; individual test entries pass. Root cause not isolated; runner not modified.
- v12.0.0.0 remains BLOCKED by missing complete Client/Hub Server/Admin source, 12-group art overlay, `FieldOperationsCatalog_v12.json`, and v12 manifests.
- Unity Editor import/compile, Play Mode, CI, APK/AAB build/install, Windows host, production TLS/WSS, pressure and soak were not run.

## Deliverables
- Word daily report: `FrontlineProtocol_Daily_Maintenance_Report_2026-11-27_Run14.docx` — 40,483 bytes; SHA-256 `436d64fcd6cf6a43e170b252a7f63ebff5085e99ab961497e16cb5ab615ca09e`.
- Word no-code update log: `FrontlineProtocol_v11.0.0.0_No_Code_Change_Update_Log_2026-11-27_Run14.docx` — 38,462 bytes; SHA-256 `56dbc18b0ae34d4f16198f938e03887c2127f7e1423bcfc09c80446929ac3859`.
- Evidence ZIP: `FrontlineProtocol_Daily_Maintenance_Evidence_2026-11-27_Run14.zip` — 84,283 bytes; 13 entries; CRC PASS; SHA-256 `59b60c49cc4048869a9dbb4e80d29ce76b0dbe490a042c4157fa1fcf2ffeb7ca`.
- No new complete source ZIP or runtime network patch generated. The 2026-11-19 runtime patch is the v10.0.0.2 -> v11.0.0.0 release overlay, not a patch to apply over an existing v11 package. The 2026-11-20 patch is test-harness only.
