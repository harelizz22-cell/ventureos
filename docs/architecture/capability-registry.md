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

## Single Ownership Rule

Every Capability has exactly one owning Domain.

Co-owned Capabilities are not allowed. If multiple Domains are involved, the work must be split into multiple Capabilities coordinated by a Workflow or the Execution Orchestrator.

## Scope Rule

Every Capability invocation must carry explicit `organization_id`, `portfolio_id`, and `venture_id` scope.

No global default Venture scope is allowed.

## Versioning Rule

Capability contracts must be versioned.

Breaking Capability contract changes require a new version, migration plan, ADR if architecturally significant, and compatibility window where required.

## Rule

Capabilities do not grant execution authority by themselves. Capability invocation is routed through Execution API, evaluated by Policy Engine, coordinated by Runtime Kernel, and governed before execution.

Agents, humans, APIs, internal services, and future execution engines may implement capabilities, but they do not define the capability architecture.

The Capability Registry is the primary architectural registry.

Capabilities never depend on specific Agents. Agents execute Capabilities.

Future execution engines must be interchangeable.

Every Capability execution path must pass through the Policy Engine. If the Policy Engine is unavailable, no Capability execution is permitted.

No Capability may bypass Execution API.

Every future capability must preserve the hierarchy:

Founder -> Organization -> Portfolio -> Venture -> Domain -> Capability -> Workflow -> Execution -> Evidence -> Decision -> Audit
