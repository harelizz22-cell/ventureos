# Observability

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for observability architecture.

## Purpose

Observability ensures meaningful actions, decisions, policy outcomes, state transitions, incidents, and production asset health can be reviewed.

## Rule

Every meaningful decision and production action must be auditable.

Audit is append-only. Audit entries cannot be edited.

Evidence, Decision, and Audit are separate architectural concerns:

- Evidence supports or challenges a claim.
- Decision records an authorized choice based on Evidence.
- Audit records what happened.

Evidence must exist before Decision. Decision without Evidence is invalid. Evidence never changes historical Decision records.
