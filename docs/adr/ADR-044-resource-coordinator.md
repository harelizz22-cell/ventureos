# ADR-044: Resource Coordinator

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Resource Coordinator decision.

## Status

Accepted

## Context

Execution must not start when required resources are unavailable. VentureOS needs pre-execution checks for budgets, AI tokens, API quotas, compute, rate limits, human approvals, capital reservations, and time windows.

## Decision

VentureOS adopts Resource Coordinator as a Runtime Kernel service.

Resource Coordinator checks resource availability before execution starts.

## Alternatives considered

- Let each Capability check resources independently.
- Defer resource checks to cost reporting after execution.
- Treat resource coordination as a business decision.

## Rationale

Central resource coordination protects cost discipline, capital discipline, rate limits, approval dependencies, and auditability.

## Risks

- Resource checks may be incomplete without clear Resource Domain boundaries.
- Resource Coordinator may be mistaken for Capital Allocation authority.
- Capital reservation dependencies may be underspecified.

## Consequences

- Required resource availability becomes a precondition for execution.
- Resource Coordinator coordinates with Resource Domain, Cost Governance, Capital Allocation Engine, Capital Reservation Model, Policy Engine, and Execution Scheduler.

## Enforcement

If required resources are unavailable, execution must not start.
