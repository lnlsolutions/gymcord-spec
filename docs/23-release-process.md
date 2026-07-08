# 23 — Release Process

## Purpose

The release process turns finished work into reliable customer value.

## Release Types

- **Patch**: bug fixes and low-risk improvements.
- **Minor**: new features that do not break existing behavior.
- **Major**: breaking changes, architecture shifts, or large product releases.
- **Hotfix**: urgent production correction.

## Release Requirements

Every release must include:

- Scope summary
- Linked pull requests
- Testing evidence
- Migration notes
- Customer impact
- Rollback plan
- Monitoring plan
- Release owner

## Release Notes

Release notes should explain what changed, who benefits, and any required customer action. Avoid internal-only language.

## Staging Review

Critical flows must be reviewed in staging before production. Billing, authentication, workouts, messaging, and permissions require special care.

## Production Monitoring

After release, monitor errors, latency, usage, conversion, billing events, notifications, and customer support signals.

## Post-Release Review

For significant releases, review adoption, incidents, customer feedback, and follow-up work.
