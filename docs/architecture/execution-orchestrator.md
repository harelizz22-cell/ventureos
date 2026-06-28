# Execution Orchestrator

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Execution Orchestrator architecture.

## Purpose

The Execution Orchestrator owns VentureOS execution flow. It coordinates execution across capabilities, workflows, approvals, events, failures, resources, assets, and recovery triggers.

## Architectural Position

VentureOS is Portfolio-first and capability-first, not agent-first. The Execution Orchestrator invokes capabilities and may route execution through AI, human, API, internal service, or future engine implementations.

## Responsibilities

- Workflow execution.
- Capability invocation.
- Governance enforcement.
- Approval waiting.
- Retry handling.
- Timeout handling.
- Failure containment.
- Event coordination.
- Recovery triggering.
- Execution state tracking.
- Resource consumption awareness.
- Asset relationship awareness.

## Execution Hierarchy

Founder -> Organization -> Portfolio -> Venture -> Domain -> Capability -> Workflow -> Execution -> Evidence -> Decision -> Audit

## Implementation Options

Implementation may be:

- AI.
- Human.
- API.
- Internal Service.
- Future Engine.

## Rules

- Agents do not own execution flow.
- CEO Agent must not orchestrate the system.
- Governance must be enforced before governed execution.
- Execution state must be auditable.
- Every meaningful execution must emit events.
- Every execution consumes Resources.
- Failed execution must be contained and routed to recovery rules when required.

## Open Questions

- What execution state model is required for Phase -1?
- What retry and timeout categories are required?
- What approval waiting states must be founder-visible?
