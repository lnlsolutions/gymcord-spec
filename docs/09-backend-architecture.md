# 09 — Backend Architecture

## Purpose

The backend powers authentication, organizations, gyms, members, trainers, programming, nutrition, messaging, billing, notifications, analytics, white-label configuration, and Atlas AI orchestration.

## Architectural Pattern

Use a modular service architecture with clear domain boundaries. Each domain owns its models, services, repositories, validation, permissions, and events.

## Core Domains

- Identity and Authentication
- Organizations and Gyms
- Members and Trainers
- Programs and Workouts
- Nutrition and Meals
- Messaging and Notifications
- Achievements, XP, Missions, and Streaks
- Billing and Subscriptions
- Analytics and Telemetry
- White-Label Configuration
- Atlas AI

## Service Layer

Services orchestrate business rules and cross-domain workflows. They should not contain database-specific query details unless isolated through repositories.

## Repository Pattern

Repositories encapsulate persistence. They expose domain-focused methods and hide raw database behavior from services.

## Context Layer

Every request should resolve actor, organization, gym, roles, permissions, feature flags, request ID, and audit context.

## Event Model

Use events for important business actions such as workout completed, mission completed, payment failed, subscription created, message sent, achievement earned, and AI recommendation generated.

## Reliability

Backend systems must support retries, idempotency, structured errors, audit logging, rate limiting, and monitoring for critical workflows.
