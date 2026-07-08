# 08 — Frontend Architecture

## Purpose

The frontend architecture supports premium member, trainer, gym, and white-label experiences across mobile and web.

## Architectural Pattern

Frontend applications should use feature-first organization with shared design-system primitives and domain-specific modules.

## Core Layers

1. **Presentation Layer**: screens, routes, layouts, and navigation.
2. **Component Layer**: reusable UI primitives and feature components.
3. **State Layer**: client state, server cache, connectivity, and optimistic updates.
4. **Service Layer**: feature orchestration and API calls.
5. **Context Layer**: auth, organization, gym, permissions, theme, connectivity, and locale.

## State Management

Use server-state tooling for remote data. Use local state for UI behavior. Use persistent local storage only for safe, intentional offline needs.

## Offline Engine

Workout execution, exercise logs, draft messages, and progress uploads should continue offline where possible. The UI must clearly communicate pending sync.

## Error Handling

Every frontend error must map to a human-readable recovery path. Silent failure is unacceptable for workouts, billing, authentication, messaging, and data sync.

## White-Label Support

Branding, color, typography accents, logo, splash screen, app name, domain, and notification identity must be tokenized and customer-configurable.

## Performance

Mobile interactions should feel immediate. Expensive screens must use skeleton states, cached data, background refresh, lazy loading, and deferred non-critical work.
