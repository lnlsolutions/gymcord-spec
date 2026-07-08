# 10 — Database Architecture

## Purpose

The database must support multi-tenant organizations, white-label gyms, members, trainers, programming, nutrition, progress, messaging, achievements, billing, and analytics.

## Entity Model

### Users
Represents authenticated people. A user may be a member, trainer, gym owner, staff member, or internal operator.

### Organizations
Top-level tenant. Owns billing, subscription, white-label configuration, gyms, users, and platform settings.

### Gyms
Physical or digital fitness locations belonging to an organization. Gyms contain members, trainers, schedules, programs, and operational reporting.

### Trainers
Coach profiles linked to users and gyms. Trainers own clients, programs, messages, progress reviews, and business analytics.

### Programs
Structured training plans assigned to members or groups. Programs contain workouts and progression rules.

### Workouts
Individual training sessions. Workouts contain exercises, sets, reps, rest periods, difficulty, equipment, and completion state.

### Exercises
Canonical movement library with videos, muscles, equipment, substitutions, coaching cues, and contraindication metadata.

### Exercise Logs
Member performance records containing sets, reps, weight, duration, tempo, RPE, notes, and completion timestamp.

### Meals
Nutrition entries containing foods, calories, macros, water, meal timing, source, and AI or coach context.

### Progress Photos
Member-uploaded visual progress records with privacy controls, timestamps, optional tags, and comparison metadata.

### Messages
Conversations between members, trainers, gyms, and Atlas AI. Messages require sender, recipient, context, read state, and audit metadata.

### Notifications
Push, email, in-app, and system notifications. Notifications require purpose, channel, delivery state, actor, and object reference.

### Achievements
Earned milestones such as personal records, streaks, consistency goals, and challenge completions.

### XP
Experience points awarded for actions. XP must be event-backed and auditable.

### Missions
Daily or weekly objectives used to guide member behavior.

### Streaks
Consistency records derived from workout, nutrition, mission, and check-in behavior.

### Subscriptions
Billing contracts for organizations, trainers, or members depending on plan type.

### Billing
Invoices, payments, payment methods, credits, discounts, tax settings, and billing events.

## Relationship Rules

- Organizations own gyms.
- Gyms belong to organizations.
- Users can belong to many organizations through memberships and roles.
- Trainers are users with trainer profiles.
- Members are users with member profiles.
- Programs belong to trainers, gyms, or organizations.
- Workouts belong to programs or are generated as standalone sessions.
- Exercise logs belong to users and workouts.
- Billing belongs to organizations unless explicitly member-billed.

## Data Requirements

Every core table must include stable IDs, timestamps, soft deletion where appropriate, tenant reference, audit metadata, and indexes for common access paths.

## Privacy

Health-adjacent data, messages, progress photos, billing, and AI context must be protected through strict permissions and minimized access.
