# 12 — Security

## Purpose

Security is a product requirement for GymCord. The platform handles identity, billing, messages, progress photos, business data, health-adjacent activity, and AI context.

## Security Principles

- Least privilege by default.
- Tenant isolation is mandatory.
- Sensitive data is minimized, encrypted, and audited.
- Security-relevant events are logged.
- External integrations are reviewed before production use.
- Secrets never live in source control.

## Data Protection

Encrypt sensitive data in transit and at rest. Treat progress photos, private messages, billing details, AI conversation context, and member performance history as high-trust data.

## Permissions

Every request must enforce actor, role, organization, gym, and resource-level access. UI hiding is not security.

## Audit Events

Audit authentication changes, role changes, billing events, data exports, AI context access, account deletion, permission changes, and administrative actions.

## Secret Management

Use managed secret stores. Rotate secrets after exposure, employee departure, vendor changes, or scheduled intervals.

## Incident Response

Every production incident must have severity, owner, timeline, customer impact, resolution, and postmortem documentation.

## Vendor Review

Vendors touching identity, payments, AI, analytics, messaging, or health-adjacent data require security and privacy review before integration.
