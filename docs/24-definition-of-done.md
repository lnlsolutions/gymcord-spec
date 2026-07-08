# 24 — Definition of Done

## Purpose

The Definition of Done ensures every feature reaches production quality before merge.

## Required Conditions

A feature is done only when all conditions are satisfied:

- The user problem is clearly solved.
- Acceptance criteria are met.
- Product behavior matches approved specification.
- UI states are complete: loading, empty, error, success, disabled, and offline where applicable.
- Permissions are enforced at backend and frontend boundaries.
- Data is validated and persisted correctly.
- Analytics and telemetry events are included where required.
- Tests cover the critical behavior.
- Documentation is updated.
- Accessibility has been reviewed.
- Security and privacy implications are addressed.
- Performance is acceptable on target devices.
- Release notes are prepared when customer-facing.

## Production Quality Rule

No feature is complete because it works once locally. It is complete when it can be trusted by real customers in production.

## Merge Rule

If a feature fails any required condition, it must not be merged unless leadership explicitly documents and accepts the risk.
