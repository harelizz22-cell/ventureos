# ADR-059: Execution Reliability

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Execution Reliability decision.

## Status

Accepted

## Context

Phase 2 requires reliability architecture before implementation. VentureOS must define how executions fail, retry, recover, escalate, and remain auditable without bypassing governance.

## Decision

VentureOS adopts Execution Reliability as the source-of-truth architecture for failure taxonomy, retry policies, idempotency, compensation, rollback, forward recovery, Dead Letter handling, timeout handling, circuit breakers, partial failure, long-running execution, recovery checkpoints, escalation, incident creation, audit, and recovery evidence.

## Alternatives considered

- Leave reliability behavior to implementation.
- Treat retries and recovery as purely technical concerns.
- Allow runtime components to retry without governance context.

## Rationale

Execution reliability must protect governance, auditability, recovery safety, policy enforcement, and Founder control before implementation begins.

## Risks

- Reliability rules may be over-applied to low-risk workflows.
- Retry and recovery rules may remain too abstract without future acceptance criteria.
- Implementation may treat reliability as infrastructure-only if governance boundaries are not preserved.

## Consequences

- Execution failures must be classified.
- Retry and recovery require idempotency, policy context, and auditability.
- Dead Letter handling, circuit breakers, timeouts, incidents, and recovery evidence become first-class reliability concerns.

## Enforcement

No future execution implementation may retry, compensate, roll back, or recover governed execution without preserving policy, scope, audit, and recovery evidence requirements.
