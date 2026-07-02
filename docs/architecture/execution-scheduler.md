# Execution Scheduler

Parent: `docs/architecture/runtime-kernel.md`

Source Of Truth: This file is the source of truth for Execution Scheduler architecture.

## Purpose

Define how VentureOS decides what execution runs, waits, pauses, or is deferred.

## Responsibilities

- Execution prioritization.
- Queue management.
- Fairness across Ventures.
- Resource-aware scheduling.
- Policy-aware scheduling.
- Cost-aware scheduling.
- Rate-limit-aware scheduling.
- Human-approval-aware scheduling.
- Emergency pause support.
- Timeout-aware scheduling.
- Long-running execution handling.
- Circuit breaker pause handling.
- Dead Letter escalation awareness.
- Token-budget-aware scheduling.
- AI cost exposure awareness.
- Runaway AI execution pause awareness.
- Workload-class-aware AI scheduling.

## Rule

Scheduler does not approve business decisions.

Scheduler only schedules already governed execution requests.

## Governance Requirements

Scheduling decisions must preserve scope, policy result, resource status, approval state, priority reason, and auditability.

Scheduling decisions for token-consuming execution must preserve token budget state, soft-limit status, hard-limit status, AI Gateway status, and escalation reason where applicable.

## Failure Modes

- Queue starvation.
- Approval wait deadlock.
- Resource exhaustion.
- Rate limit exhaustion.
- Emergency pause.
- Circuit breaker open.
- Dead Letter threshold reached.
- Long-running execution checkpoint missing.
- Token hard limit reached.
- Runaway token-consuming execution detected.
- AI Gateway cannot provide token usage forecast or usage record.

## Reliability Requirements

The Scheduler may only retry, resume, or reschedule execution when retry eligibility, idempotency, policy context, resource availability, and approval requirements are known.

The Scheduler must respect circuit breaker state, timeout policy, recovery checkpoints, and emergency pause status.

The Scheduler must also respect AI token hard limits, Founder approval thresholds, emergency override expiry, and token budget availability.

Discovery / Research scheduling may allow longer or larger token-consuming work than strict workload classes, but must preserve monitoring, checkpoints, escalation thresholds, and stop conditions for runaway loops.

## Approval Validity Scheduling

Execution Scheduler must not start work from an expired approval.

Before execution start, Scheduler must confirm approval TTL, policy snapshot validity, resource check validity, token reservation state, capital reservation state where applicable, and required human approval status.

If a resource check fails after approval, Scheduler must cancel, requeue, or route the request for re-evaluation. It must not start execution based on stale approval.

## Scheduler Fairness Model

Scheduler must preserve fairness across Ventures, Portfolios, and governed priority classes.

Fairness policy must balance:

- Weighted priority.
- Emergency priority.
- Recovery priority.
- Starvation prevention.
- Venture fairness.
- Portfolio fairness.
- Treasury-sensitive priority handling.

Weighted priority may consider policy urgency, approval age, business impact, recovery state, resource reservation expiry, and Founder-visible urgency.

Emergency priority may preempt ordinary execution only to restrict risk, preserve audit, prevent loss, or protect capital. Emergency priority must not expand authority.

Recovery priority may move governed recovery work ahead of ordinary execution when needed to restore safety, preserve audit, release reservations, or resolve incidents.

Starvation prevention must detect requests that remain queued too long and require re-prioritization, escalation, or explicit explanation.

Venture fairness prevents a single Venture from consuming disproportionate execution capacity unless policy-approved priority justifies it.

Portfolio fairness prevents one Portfolio from starving another Portfolio unless approved governance priority justifies it.

Treasury-sensitive priority handling may prioritize reservation expiry, capital-risk events, budget conflict resolution, and financial incident recovery, but it does not approve capital actions or money movement.

## Placeholder Status

This is architecture documentation only. It does not define queues, services, infrastructure, algorithms, or implementation.
