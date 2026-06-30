# ADR-057: Event Ordering And Replay Model

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Event Ordering and Replay Model decision.

## Status

Accepted

## Context

VentureOS is Event-first. Before implementation, it must define ordering, deduplication, replay, schema versioning, duplicate handling, out-of-order handling, audit behavior, and recovery usage.

## Decision

VentureOS adopts the Event Ordering and Replay Model for governed Event ordering, per-entity ordering, deduplication, replay, schema versioning, duplicate handling, out-of-order handling, replay audit, and recovery usage.

## Alternatives considered

- Treat Events as unordered logs.
- Allow replay to rewrite historical Decisions.
- Handle duplicate and out-of-order Events only during implementation.

## Rationale

Event ordering and replay rules protect audit integrity, recovery, observability, and future runtime correctness.

## Risks

- Per-entity ordering may be complex across many scopes.
- Replay may be misunderstood as historical mutation.
- Duplicate handling may hide meaningful incidents if not audited.

## Consequences

- Event replay must preserve audit integrity.
- Historical Decisions must not be rewritten.
- Duplicate and out-of-order Events require defined behavior before implementation.

## Enforcement

Replay, duplicate handling, and out-of-order handling must preserve Event, Evidence, Decision, Audit, and Recovery boundaries.
