# 11 — API Standards

## Purpose

GymCord APIs must be predictable, secure, documented, versioned, and easy for frontend, mobile, AI, and future integration clients to consume.

## API Principles

- Use consistent resource naming.
- Validate all input at boundaries.
- Return structured errors.
- Require authentication by default.
- Enforce tenant and role permissions on every request.
- Use idempotency for payments, retries, sync, and mutations that may be repeated.

## Resource Naming

Use plural nouns for resource collections. Use stable IDs rather than names in paths.

Examples:

```text
/organizations/{organizationId}/gyms
/gyms/{gymId}/members
/members/{memberId}/workouts
/workouts/{workoutId}/logs
```

## Response Shape

Responses should include `data`, `meta`, and `errors` where appropriate. Pagination must be cursor-based for large collections.

## Error Shape

Errors must include code, message, request ID, recoverability, and field-level details when validation fails.

## Versioning

Public API changes must be versioned. Breaking changes require migration documentation and deprecation windows.

## Rate Limiting

Rate limits must protect authentication, messaging, AI generation, billing, and public endpoints.

## Documentation

Every API must document purpose, authentication, permissions, request fields, response fields, error cases, rate limits, and example payloads.
