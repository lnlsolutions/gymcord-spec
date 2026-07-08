# 07 — Repository Structure

## Purpose

GymCord uses separate repositories to keep responsibilities clean while preserving shared standards through this specification.

## Repository Types

- `gymcord-spec`: documentation-only master specification.
- `gymcord-mobile`: member, trainer, and gym mobile application surfaces.
- `gymcord-web`: web dashboard, admin, marketing, and customer portals.
- `gymcord-api`: backend API, orchestration, authentication, billing, and platform services.
- `gymcord-atlas`: AI prompt architecture, memory services, evaluation, and safety documentation or implementation.
- `gymcord-design`: design tokens, assets, and component references.
- `gymcord-infra`: deployment, environments, cloud configuration, monitoring, and CI/CD workflows.

## Shared Standards

Every repository must include:

- `README.md`
- `docs/` for repository-specific documentation
- `CONTRIBUTING.md`
- `SECURITY.md`
- Environment documentation
- Testing commands
- Release instructions

## Versioning

Repositories should use semantic versioning for release artifacts and dated decision logs for architecture changes.

## Ownership

Every repository must have a clear owner. Ownership includes documentation accuracy, review standards, security posture, and release readiness.

## Cross-Repository Changes

Changes spanning multiple repositories must include a coordination plan, migration order, rollback plan, and acceptance criteria before implementation begins.
