# Agent Registry

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Agent Registry architecture.

## Purpose

The Agent Registry is a runtime implementation registry only. It is secondary to the Capability Registry.

It stores approved agents, responsibilities, constraints, inputs, outputs, escalation rules, and activation status.

Agents are implementation details for capabilities. They are not the primary architecture model.

AI is not the product. AI Agents are one implementation option among humans, APIs, internal services, and future execution engines.

## Agent Identity Requirements

Agents are first-class identities in the Identity Domain.

Agents are not anonymous code acting on behalf of a human.

Every Agent Registry record must connect to an Identity record and define:

- Allowed scope.
- Autonomy ceiling.
- Capability permissions.
- Audit attribution.

## Rule

Agents cannot modify their own contract, approve themselves, or grant themselves new capabilities.

Agents do not own execution flow. Execution flow belongs to `docs/architecture/execution-orchestrator.md`.

Agents execute Capabilities. Capabilities never depend on specific Agents.

Agents may not self-approve execution. Agent execution paths must enter through Execution API and pass through the Policy Engine.

Agents may participate in Dynamic Review Council, Debate Engine, Consensus Engine, and Investment Memo preparation, but they do not self-approve, make final decisions, or bypass Evidence requirements.
