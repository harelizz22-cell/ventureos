# ADR-094: Scheduler Fairness Model

Parent: `docs/architecture/execution-scheduler.md`

Status: Accepted

## Context

Execution scheduling needs fairness across Ventures and Portfolios while still respecting emergency, recovery, and treasury-sensitive priorities.

## Decision

Adopt scheduler fairness policy, weighted priority, emergency priority, recovery priority, starvation prevention, Venture fairness, Portfolio fairness, and treasury-sensitive priority handling.

## Alternatives

- Use first-in-first-out scheduling only.
- Let highest priority always win.
- Leave fairness to implementation.

## Rationale

Fairness protects portfolio operations from starvation and priority abuse.

## Risks

Fairness rules can add scheduling complexity.

## Consequences

Execution Scheduler and Execution Reliability must treat unfair queue behavior as an operational risk.

## Enforcement

Emergency priority may restrict execution but must not expand authority; starvation requires visibility, escalation, or rebalancing.
