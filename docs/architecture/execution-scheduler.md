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

## Placeholder Status

This is architecture documentation only. It does not define queues, services, infrastructure, algorithms, or implementation.
