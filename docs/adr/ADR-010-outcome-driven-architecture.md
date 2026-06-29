# ADR-010: Outcome-Driven Architecture

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted outcome-driven architecture decision.

## Status

Accepted

## Context

VentureOS must not optimize for tasks, workflows, agents, or technical activity. The system exists to create measurable business value.

## Decision

VentureOS is outcome-driven.

Every Capability must contribute toward measurable business outcomes. Every Workflow must exist because it creates business value. Every autonomous action must be traceable to a measurable objective.

## Consequences

- Capabilities require business outcome context.
- Workflows require value rationale.
- Autonomous actions require measurable objectives.
- Technical activity is not success by itself.

## Enforcement

Architecture, phase specifications, and future implementation planning must reject task-driven, workflow-driven, or agent-driven success criteria.

