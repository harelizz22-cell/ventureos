# Capability Registry

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Capability Registry architecture.

## Purpose

The Capability Registry is the primary execution planning registry. It defines system capabilities independently from agents or implementation mechanisms.

VentureOS is capability-first, not agent-first.

## Required Capability Attributes

- Purpose.
- Risk class.
- Dependencies.
- Required approvals.
- Allowed tools.

## Rule

Capabilities do not grant execution authority by themselves. Capability invocation is routed through the Execution Orchestrator and governed before execution.

Agents, humans, APIs, internal services, and future execution engines may implement capabilities, but they do not define the capability architecture.
