# Capability Registry

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Capability Registry architecture.

## Purpose

The Capability Registry is the primary execution planning registry. It defines system capabilities independently from agents or implementation mechanisms.

VentureOS is capability-first, not agent-first.

Capabilities belong to Domains and must be multi-venture aware.

## Required Capability Attributes

- Purpose.
- Risk class.
- Dependencies.
- Required approvals.
- Allowed tools.
- Owning Domain.
- Portfolio and Venture awareness.
- Resource requirements.
- Event requirements.

## Rule

Capabilities do not grant execution authority by themselves. Capability invocation is routed through the Execution Orchestrator and governed before execution.

Agents, humans, APIs, internal services, and future execution engines may implement capabilities, but they do not define the capability architecture.

The Capability Registry is the primary architectural registry.

Capabilities never depend on specific Agents. Agents execute Capabilities.

Future execution engines must be interchangeable.

Every Capability execution path must pass through the Policy Engine. If the Policy Engine is unavailable, no Capability execution is permitted.

Every future capability must preserve the hierarchy:

Founder -> Organization -> Portfolio -> Venture -> Domain -> Capability -> Workflow -> Execution -> Evidence -> Decision -> Audit
