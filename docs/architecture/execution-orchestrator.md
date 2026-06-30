# Execution Orchestrator

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Execution Orchestrator architecture.

## Purpose

The Execution Orchestrator owns VentureOS execution flow. It coordinates execution across capabilities, workflows, approvals, events, failures, resources, assets, and recovery triggers.

## Architectural Position

VentureOS is Portfolio-first and capability-first, not agent-first. The Execution Orchestrator invokes capabilities and may route execution through AI, human, API, internal service, or future engine implementations.

Execution Orchestrator is now decomposed under VentureOS Runtime Kernel.

Runtime Kernel services are documented in `docs/architecture/runtime-kernel.md`.

All Capability execution requests must enter through `docs/architecture/execution-api.md`.

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
- Runtime Kernel runs the system but does not make business decisions.
- Governance must be enforced before governed execution.
- No Capability, Agent, Tool, Workflow, Service, or external provider may bypass Execution API.
- All execution paths must pass through the Policy Engine.
- No Capability, Agent, Workflow, Tool, Service, or External Provider may self-approve execution.
- If the Policy Engine is unavailable, VentureOS must fail closed.
- No execution is permitted while governance is unavailable.
- Execution state must be auditable.
- Every meaningful execution must emit events.
- Every execution consumes Resources.
- Cost Governance may be used as a Policy Engine approval input.
- Failed execution must be contained and routed to recovery rules when required.
- At startup, execution requests must not be accepted until Policy Engine health is confirmed.
- If the Policy Engine becomes unavailable, new execution must stop fail-closed.

## Policy Response Handling

Policy Engine decision outcomes are Approved, Denied, Pending Founder Approval, Pending Delegated Approval, Blocked By Governance, and Fail Closed.

The Execution Orchestrator owns waiting and continuation behavior after Policy Engine response.

## Profit Awareness

The Execution Orchestrator must eventually become cost-aware.

Future execution path selection may consider:

- Policy.
- Quality.
- Latency.
- Cost.
- Expected business value.

The cheapest execution is not always correct. The most expensive execution is not always justified.

## Open Questions

- What execution state model is required for Phase -1?
- What retry and timeout categories are required?
- What approval waiting states must be founder-visible?
