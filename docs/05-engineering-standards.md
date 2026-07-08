# 05 — Engineering Standards

## Purpose

GymCord engineering standards define how production systems are designed, reviewed, tested, documented, and maintained.

## Core Standards

- Use TypeScript for application code.
- Prefer explicit types for public interfaces, domain entities, API contracts, and service boundaries.
- Keep business logic out of UI components.
- Use service layers for orchestration and repository layers for persistence.
- Use context layers for authenticated user, organization, gym, feature flags, theme, locale, and permissions.
- Document non-obvious decisions in Architecture Decision Records.

## Naming

Names should describe business meaning, not implementation shortcuts. Use consistent domain language: Member, Trainer, Gym, Organization, Program, Workout, Exercise, Mission, Achievement, Subscription.

## TypeScript

Use strict mode. Avoid `any` unless explicitly isolated at system boundaries. Validate external data before it enters domain logic.

## React

Components should be small, composable, and predictable. Screen components orchestrate layout. Feature components handle domain-specific presentation. Shared components remain generic and token-driven.

## Testing

Tests must cover core logic, permissions, payments, authentication, synchronization, API contracts, and critical user flows.

## Documentation

Every module must explain purpose, ownership, inputs, outputs, dependencies, and failure modes. Documentation is part of the product.

## Git

All production changes must go through a pull request. Branches should be short-lived and named by purpose: `feature/`, `fix/`, `docs/`, `chore/`, or `release/`.

## Review Requirements

A pull request is not ready unless it includes scope, implementation summary, testing evidence, screenshots for UI changes, migration notes when applicable, and known risks.
