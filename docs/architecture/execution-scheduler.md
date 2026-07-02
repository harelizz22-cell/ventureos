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

## Placeholder Status

This is architecture documentation only. It does not define queues, services, infrastructure, algorithms, or implementation.
