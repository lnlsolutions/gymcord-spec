# 03 — Design System

## Purpose

The GymCord design system defines the visual and interaction foundation used across mobile, web, trainer, gym, and white-label experiences.

## Typography

Use a modern sans-serif system optimized for readability. Headings should feel confident and premium. Body copy should be clear at small sizes. Numeric values for workouts, analytics, nutrition, and progress must use tabular alignment where supported.

## Spacing

Use an 8-point spacing system. Mobile screens should breathe. Dense dashboards are allowed only when hierarchy remains clear.

## Radius

Cards, inputs, and primary buttons should use generous rounded corners. Radius communicates softness and approachability while preserving a premium product feel.

## Elevation

Use subtle elevation. Shadows should create hierarchy, not decoration. Dark mode surfaces should rely more on contrast and layering than heavy shadows.

## Animation and Motion

Motion must be fast, smooth, and purposeful. Use animation to confirm completion, reveal progress, guide attention, and celebrate achievement. Avoid slow, decorative animations that block action.

## Color System

GymCord should be dark-mode first with strong white-label support.

Core semantic roles:

- **Success**: progress, completion, streaks, goals.
- **Warning**: recovery risk, missed workouts, billing issues.
- **Danger**: destructive actions, security warnings.
- **Info**: guidance, coaching, system explanation.
- **Neutral**: surfaces, borders, text, disabled states.

Brand colors must be tokenized so each gym can apply custom themes without breaking accessibility.

## Component Standards

Every component must define usage, states, variants, accessibility behavior, empty behavior, loading behavior, and error behavior.

Required states:

- Default
- Hover where applicable
- Pressed
- Focused
- Disabled
- Loading
- Error
- Success

## Accessibility

All components must support large touch targets, readable contrast, keyboard interaction where applicable, screen reader labels, dynamic text sizing, and colorblind-safe meaning indicators.
