# 13 — Authentication

## Purpose

Authentication controls identity, access, trust, and tenant safety across GymCord.

## Identity Model

A user account represents a person. Roles are assigned through organization and gym memberships. A person may be a member in one organization, a trainer in another, and an admin in a third.

## Required Auth Capabilities

- Email and password authentication
- Magic link or passwordless support where appropriate
- OAuth providers when strategically valuable
- Multi-factor authentication for admins and internal operators
- Session management
- Device management
- Password reset
- Account recovery
- Account deletion

## Authorization Context

Every authenticated request must resolve:

- User ID
- Organization ID
- Gym ID where applicable
- Role
- Permissions
- Feature flags
- Subscription state
- Request ID

## Session Rules

Sessions should expire based on risk and role. Admin and billing actions should require stronger confirmation than routine member actions.

## Role Examples

- Member
- Trainer
- Gym Staff
- Gym Owner
- Organization Admin
- GymCord Operator
- Support Agent

## Security Requirements

Authentication flows must protect against brute force, credential stuffing, session fixation, CSRF where applicable, token leakage, and insecure redirects.

## User Experience

Authentication must feel fast and trustworthy. Error messages should be secure, helpful, and not reveal sensitive account existence details.
