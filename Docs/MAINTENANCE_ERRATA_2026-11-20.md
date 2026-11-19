# Maintenance Errata — 2026-11-20

## TEST-WS-001 — asynchronous snapshot race in the regression harness

**Observed:** Tests/maintenance_regression_test.py sent a WebSocket command and asserted against only the next received frame. The server emits periodic snapshot frames at 10 Hz, so a legal snapshot could arrive before the command response and cause a false failure.

**Correction:** Added recv_expected(ws, expected_type, timeout=5.0). It ignores only snapshot frames, waits for the requested event, fails on any other unexpected event, and fails on timeout. Applied to welcome, shoot rejection, input errors and pong checks.

**Scope:** Test harness only. No runtime server/client code, network message schema, API, protocol, configuration, Admin Panel or art asset changed. This is not counted as a runtime bug fix and does not increment the four-segment formal version.

**Verification:** 16/16 regression entry points passed individually after the correction; the corrected maintenance regression also passed five consecutive standalone runs.
