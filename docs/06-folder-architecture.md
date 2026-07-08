# 06 — Folder Architecture

## Purpose

This document defines the preferred folder architecture for future GymCord application repositories.

## Standard Application Layout

```text
src/
  app/
  assets/
  components/
  config/
  contexts/
  database/
  design-system/
  features/
  hooks/
  lib/
  modules/
  repositories/
  routes/
  services/
  stores/
  styles/
  telemetry/
  tests/
  types/
  utils/
```

## Layer Responsibilities

- `app/` contains application bootstrap, providers, route registration, and platform setup.
- `components/` contains reusable UI components with no business ownership.
- `design-system/` contains tokens, primitives, component standards, and theme logic.
- `features/` contains user-facing feature flows such as onboarding, dashboard, workout engine, messaging, and billing.
- `modules/` contains domain modules such as member, trainer, gym, atlas, billing, analytics, and white-label.
- `repositories/` contains persistence access patterns.
- `services/` contains business orchestration and external integrations.
- `contexts/` contains app-wide state such as auth, organization, permissions, theme, and connectivity.
- `telemetry/` contains event schemas, logging, monitoring, and analytics tracking.

## Rule

A file belongs where its responsibility lives. If a file knows about UI, business rules, database access, and external APIs at the same time, the architecture is wrong.
