# Observability

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for observability architecture.

## Purpose

Observability ensures meaningful actions, decisions, policy outcomes, state transitions, incidents, and production asset health can be reviewed.

## Rule

Every meaningful decision and production action must be auditable.

Observability must support business health, not only technical status. Founder-facing observability must make money, risk, growth, approvals, blockers, daily change, and expected outcomes visible without requiring log inspection.

Audit is append-only. Audit entries cannot be edited.

Evidence, Decision, and Audit are separate architectural concerns:

- Evidence supports or challenges a claim.
- Decision records an authorized choice based on Evidence.
- Audit records what happened.

Evidence must exist before Decision. Decision without Evidence is invalid. Evidence never changes historical Decision records.

## Observability To Evidence Bridge

Observability signals may be promoted to Evidence for Decisions only through a governed promotion process.

Raw telemetry must not automatically become Evidence.

Example: Agent error rate may become Evidence for Agent deprecation after governed promotion.

## Execution Reliability Observability

Observability must support Execution Reliability Metrics, including success rate, failure rate, retry rate, recovery success rate, mean recovery time, execution latency, timeout frequency, Dead Letter volume, and incident frequency.

Reliability metrics are observability signals. They may become Evidence for Decisions only through governed Evidence Promotion.

Incident, recovery, retry, timeout, circuit breaker, and Dead Letter signals must preserve scope, policy snapshot, correlation, causation, and audit references where meaningful.
