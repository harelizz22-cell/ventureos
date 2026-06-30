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

## Rule

Scheduler does not approve business decisions.

Scheduler only schedules already governed execution requests.

## Governance Requirements

Scheduling decisions must preserve scope, policy result, resource status, approval state, priority reason, and auditability.

## Failure Modes

- Queue starvation.
- Approval wait deadlock.
- Resource exhaustion.
- Rate limit exhaustion.
- Emergency pause.
- Circuit breaker open.
- Dead Letter threshold reached.
- Long-running execution checkpoint missing.

## Reliability Requirements

The Scheduler may only retry, resume, or reschedule execution when retry eligibility, idempotency, policy context, resource availability, and approval requirements are known.

The Scheduler must respect circuit breaker state, timeout policy, recovery checkpoints, and emergency pause status.

## Placeholder Status

This is architecture documentation only. It does not define queues, services, infrastructure, algorithms, or implementation.
