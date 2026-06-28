# Agent Registry

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Agent Registry architecture.

## Purpose

The Agent Registry is a runtime implementation registry only. It is secondary to the Capability Registry.

It stores approved agents, responsibilities, constraints, inputs, outputs, escalation rules, and activation status.

Agents are implementation details for capabilities. They are not the primary architecture model.

AI is not the product. AI Agents are one implementation option among humans, APIs, internal services, and future execution engines.

## Rule

Agents cannot modify their own contract, approve themselves, or grant themselves new capabilities.

Agents do not own execution flow. Execution flow belongs to `docs/architecture/execution-orchestrator.md`.

Agents execute Capabilities. Capabilities never depend on specific Agents.

Agents may not self-approve execution. Agent execution paths must pass through the Policy Engine.
