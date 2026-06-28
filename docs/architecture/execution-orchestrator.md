# Execution Orchestrator

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Execution Orchestrator architecture.

## Purpose

The Execution Orchestrator owns VentureOS execution flow. It coordinates execution across capabilities, workflows, approvals, events, failures, and recovery triggers.

## Architectural Position

VentureOS is capability-first, not agent-first. The Execution Orchestrator invokes capabilities and may route execution through an AI agent, human, external API, internal service, or future execution engine.

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

## Execution Hierarchy

Domain -> Capability -> Workflow -> Execution -> Implementation

## Implementation Options

Execution may be performed by:

- AI Agent.
- Human.
- External API.
- Internal service.
- Future execution engine.

## Rules

- Agents do not own execution flow.
- CEO Agent must not orchestrate the system.
- Governance must be enforced before governed execution.
- Execution state must be auditable.
- Failed execution must be contained and routed to recovery rules when required.

## Open Questions

- What execution state model is required for Phase -1?
- What retry and timeout categories are required?
- What approval waiting states must be founder-visible?

