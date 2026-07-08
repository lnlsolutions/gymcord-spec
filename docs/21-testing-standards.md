# 21 — Testing Standards

## Purpose

Testing protects trust, revenue, safety, and product quality.

## Required Test Types

- Unit tests for domain logic
- Integration tests for services, repositories, and APIs
- Contract tests for frontend-backend boundaries
- End-to-end tests for critical user journeys
- Accessibility tests for core UI
- Permission tests for tenant and role boundaries
- Regression tests for previously fixed production issues

## Critical Flows

The following flows require strong test coverage:

- Authentication
- Onboarding
- Workout execution and logging
- Offline sync
- Messaging
- Billing
- Subscription state
- Role and permission changes
- Progress photo privacy
- AI recommendation safety
- White-label theme rendering

## Test Data

Test data must reflect real domain complexity: multiple organizations, gyms, roles, members, trainers, subscriptions, and permission boundaries.

## Quality Rule

A feature without meaningful tests is not production ready. Tests must prove behavior, not simply increase coverage numbers.
