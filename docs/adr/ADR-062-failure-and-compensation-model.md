# ADR-062: Failure And Compensation Model

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Failure and Compensation Model decision.

## Status

Accepted

## Context

VentureOS needs a clear model for partial failures, compensation, rollback, forward recovery, Dead Letter handling, and incident creation before implementation.

## Decision

VentureOS adopts a governed Failure and Compensation Model. Failures must be classified, partial completion must remain visible, compensation must preserve audit history, rollback must not rewrite history, and forward recovery must be governed.

## Alternatives considered

- Treat all failures as generic execution failures.
- Prefer rollback for all failures.
- Allow compensation to hide the original failed action.

## Rationale

Different failure types require different recovery paths. Preserving partial state, audit history, and compensation records protects trust and recovery correctness.

## Risks

- Compensation paths may be hard to define before implementation.
- Rollback may be overused even when forward recovery is safer.
- Dead Letter records may become ignored unless observability and escalation are enforced.

## Consequences

- Failure taxonomy becomes mandatory for governed execution.
- Compensation and rollback are governed actions.
- Dead Letter and incident rules become part of execution reliability architecture.

## Enforcement

Compensation, rollback, and forward recovery must preserve Evidence, Decision, Audit, Policy, Event, and Recovery Governance boundaries.
