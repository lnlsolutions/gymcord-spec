# 22 — CI/CD

## Purpose

CI/CD ensures GymCord releases are repeatable, tested, secure, and traceable.

## Required CI Checks

Every pull request must run:

- Type checking
- Linting
- Unit tests
- Integration tests where applicable
- Build verification
- Security scanning
- Dependency review
- Formatting checks
- Documentation link checks for documentation repositories

## Environments

Use separate environments for development, staging, preview, and production. Production credentials and data must never be used in development.

## Preview Deployments

Frontend and documentation changes should generate preview links when possible. Reviewers should validate behavior visually before merge.

## Deployment Rules

Deployments must be automated, logged, and reversible. Manual production changes are allowed only in controlled incidents and must be documented afterward.

## Secrets

CI/CD secrets must be stored in approved secret-management systems. They must not be echoed in logs, committed, or shared in chat.

## Rollback

Every production deployment must have a rollback strategy. Database migrations require forward and backward safety analysis.

## Release Evidence

Each release must preserve commit SHA, author, environment, timestamp, tests, approvals, and deployment status.
