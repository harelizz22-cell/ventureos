# ADR-007: Event-Driven Architecture

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted event-driven architecture decision.

## Status

Accepted

## Context

VentureOS needs auditability, loose coupling, recovery, observability, and future autonomy across many Organizations, Portfolios, Ventures, Capabilities, and Executions.

## Decision

VentureOS adopts an Event-first runtime. Everything meaningful emits events.

Future systems must subscribe to events instead of tightly coupling services.

## Event Examples

- Organization Created
- Portfolio Created
- Venture Created
- Capability Registered
- Capability Executed
- Workflow Started
- Workflow Completed
- Evidence Added
- Decision Approved
- Policy Violated
- Asset Registered
- Incident Raised
- Recovery Started
- Audit Recorded
- Execution Failed
- Execution Retried

## Consequences

- Event architecture is first-class.
- Meaningful runtime behavior must emit auditable events.
- Event contracts must precede implementation.
- Recovery, audit, observability, and future autonomy depend on event integrity.

## Enforcement

Architecture and phase specifications must identify meaningful events before implementation.

