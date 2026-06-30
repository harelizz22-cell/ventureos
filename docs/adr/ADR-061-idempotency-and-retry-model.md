# ADR-061: Idempotency And Retry Model

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Idempotency and Retry Model decision.

## Status

Accepted

## Context

Retries can create duplicate side effects, duplicate external calls, audit confusion, and capital or asset risk unless idempotency and retry limits are defined before implementation.

## Decision

VentureOS adopts an idempotency-first retry model. Retryable execution must define idempotency identity, retry limits, backoff, retry audit, policy context, and escalation rules.

## Alternatives considered

- Retry failed operations without idempotency proof.
- Let each Capability define retry behavior independently.
- Use retry as the default recovery path for all failures.

## Rationale

Idempotency protects state integrity, audit integrity, external side effects, and governed recovery.

## Risks

- Some operations may not be safely retryable.
- Idempotency keys may be hard to define for multi-step workflows.
- Retry policies may mask deeper dependency failures if circuit breakers and escalation are weak.

## Consequences

- If idempotency cannot be proven, retry must be blocked or escalated.
- Retry policies must preserve Policy Engine, approval, resource, compliance, and audit requirements.
- Retry backoff and circuit breakers become required reliability design concerns.

## Enforcement

No retry may proceed for governed execution unless retry eligibility, idempotency, policy context, retry limit, and audit behavior are established.
