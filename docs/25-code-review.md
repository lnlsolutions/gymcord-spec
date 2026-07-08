# 25 — Code Review

## Purpose

Code review protects quality, security, maintainability, and shared understanding.

## Review Standards

Reviewers must evaluate:

- Product behavior
- Architecture alignment
- Data handling
- Security and permission logic
- Error handling
- Test coverage
- Naming and readability
- Performance
- Accessibility for UI changes
- Documentation accuracy

## Pull Request Requirements

Every pull request must include:

- Clear summary
- Reason for change
- Screenshots or recordings for UI work
- Testing evidence
- Risk notes
- Rollback or mitigation plan for risky changes
- Linked issue or specification when available

## Review Behavior

Reviews should be direct, respectful, specific, and outcome-focused. Comments should explain the risk or reasoning behind requested changes.

## Approval Rule

Approval means the reviewer believes the change is safe, understandable, aligned with GymCord standards, and ready to ship under the stated scope.

## Blocking Issues

Security gaps, missing permission enforcement, broken critical flows, untested billing changes, unclear data migrations, and undocumented architecture changes block merge.
