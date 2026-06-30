# ADR-043: Execution Scheduler

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Execution Scheduler decision.

## Status

Accepted

## Context

VentureOS needs governed scheduling behavior for execution priority, queues, fairness across Ventures, resources, cost, rate limits, approvals, and emergency pause support.

## Decision

VentureOS adopts Execution Scheduler as a Runtime Kernel service.

Execution Scheduler schedules already governed execution requests.

## Alternatives considered

- Let execution order be implicit.
- Let Agents choose execution priority.
- Merge scheduling with business recommendation logic.

## Rationale

Scheduling is runtime coordination, not business judgment. Separating scheduling prevents runtime mechanics from becoming hidden business approval.

## Risks

- Scheduler priority rules may accidentally encode strategy.
- Fairness across Ventures may be under-specified.
- Resource-aware scheduling may be mistaken for capital approval.

## Consequences

- Execution prioritization, queues, fairness, resources, policy, cost, rate limits, approvals, and emergency pauses become architecture concerns.
- Scheduler does not approve business decisions.

## Enforcement

Scheduler only schedules already governed execution requests and must not approve business decisions.
