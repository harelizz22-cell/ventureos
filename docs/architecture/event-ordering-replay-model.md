# Event Ordering And Replay Model

Parent: `docs/architecture/event-architecture.md`

Source Of Truth: This file is the source of truth for Event ordering and replay architecture.

## Purpose

Define how VentureOS orders, deduplicates, versions, replays, and audits Events without weakening Decision, Evidence, or Audit integrity.

## Event Ordering Model

Events are meaningful runtime facts.

VentureOS must preserve enough ordering context to reconstruct what happened within the relevant Organization, Portfolio, Venture, Domain, Capability, Workflow, Execution, Evidence, Decision, Audit, and Recovery scope.

## Per-Entity Ordering

Per-entity ordering must be preserved where meaningful.

Entity scope may include:

- Organization
- Portfolio
- Venture
- Domain
- Capability
- Workflow
- Execution
- Evidence record
- Decision record
- Asset
- Recovery incident

## Deduplication

Duplicate Events must be detected by stable identifiers and context.

Deduplication must not delete audit history. It must record duplicate detection behavior where meaningful.

## Replay

Replay is the governed reprocessing of historical Events for recovery, rebuilding read models, audit review, analysis, or migration.

Replay must not rewrite historical Decisions, Evidence, or Audit records.

## Schema Versioning

Event payloads must include schema version.

Breaking changes require a new version, migration plan, ADR if architecturally significant, and compatibility window where required.

## Duplicate Event Handling

Duplicate Events should be ignored for state mutation where already applied, but duplicate observation should remain auditable where meaningful.

## Out-Of-Order Event Handling

Out-of-order Events must not silently corrupt state.

Out-of-order behavior may include:

- Holding the Event
- Reordering within allowed bounds
- Marking as late
- Requiring recovery
- Escalating for review
- Failing closed for governed execution

## Audit Behavior For Replayed Events

Replayed Events must be marked as replayed.

Audit must preserve:

- Original Event identity
- Replay time
- Replay reason
- Replay actor or component
- Replay scope
- Replay result

## Recovery Usage

Recovery Manager may use Event replay to rebuild state, diagnose incidents, coordinate compensation, or verify recovery.

Recovery replay must preserve governance, Evidence, Decision, and Audit boundaries.

Recovery replay must follow `docs/architecture/recovery-governance.md` and must preserve recovery audit, recovery evidence, original Event identity, policy snapshot, and replay reason.

## Rule

Event replay must preserve audit integrity and must not rewrite historical Decisions.

## Placeholder Status

This is architecture documentation only. It does not define event stores, queues, schemas, services, APIs, infrastructure, or implementation.
