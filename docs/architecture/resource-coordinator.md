# Resource Coordinator

Parent: `docs/architecture/runtime-kernel.md`

Source Of Truth: This file is the source of truth for Resource Coordinator architecture.

## Purpose

Define resource availability checks before execution starts.

## Responsibilities

- Budget availability check.
- AI token budget check.
- API quota check.
- Compute availability check.
- Rate limit check.
- Human approval dependency check.
- Capital reservation dependency check.
- Time-window validation.
- Token budget scope validation.
- Token soft-limit and hard-limit validation.
- Token usage forecast review.
- Token workload class validation.
- Discovery / Research flexible budget validation.

## Coordination

Resource Coordinator coordinates with:

- Resource Domain.
- Cost Governance.
- Capital Allocation Engine.
- Capital Reservation Model.
- Policy Engine.
- Execution Scheduler.
- AI Gateway.
- AI Token Governance.
- Treasury Domain.

## Rule

If required resources are unavailable, execution must not start.

## Governance Requirements

Resource checks must be scoped, auditable, policy-aware, and cost-aware where meaningful.

Resource Coordinator may block execution or request escalation. It does not approve business strategy, capital allocation, or money movement.

AI token checks must be scoped to Organization, Portfolio, Venture, Capability, Agent, and Execution.

Resource Coordinator must not allow high-cost AI execution to start when token budget state is unavailable, attribution is missing, hard limits are reached, or required Founder approval is absent.

Discovery / Research workloads may receive larger soft-budget breathing room, but Resource Coordinator must still require attribution, monitoring, hard limits, escalation thresholds, and stop conditions for runaway loops.

## Approval And Resource Re-Validation

Resource Coordinator must re-check required resources after approval and before execution start.

If resource availability changes after approval, execution must not start until the request is cancelled, requeued, or re-evaluated with current resource context.

Approval TTL does not preserve stale resource availability.

Resource checks must include capital reservation, token reservation, quota, rate limit, compute, human dependency, and time-window status where applicable.

## Token Budget Reservation

Token-consuming execution must reserve token budget before execution starts when policy requires reservation.

Token reservation records must include Organization, Portfolio, Venture, Capability, Agent, Execution, workload class, budget source, reservation amount, expiry, release conditions, and correlation ID.

Reservation expiry releases unused reserved tokens back to the applicable budget scope.

Reservation release must occur when execution completes, is cancelled, fails before consumption, is requeued, or expires.

Over-consumption must stop, pause, or escalate execution according to hard limits, approved override, and Policy Engine outcome.

Race conditions must be handled by treating reservation state as authoritative. If concurrent requests would exceed the most restrictive applicable limit, the later or lower-priority request must wait, requeue, or fail closed.

Inheritance and override order:

Organization -> Portfolio -> Venture -> Capability -> Agent -> Execution

The most restrictive applicable limit wins unless an approved governance override exists.

## Placeholder Status

This is architecture documentation only. It does not define resource schemas, quotas, integrations, services, or implementation.
