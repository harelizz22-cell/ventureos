# VentureOS Architecture

Parent: `docs/project/ventureos-system-bible.md`

Source Of Truth: This file is the technical architecture index for VentureOS.

## Purpose

This document identifies the source of truth for each technical architecture concern. It does not replace concern-specific architecture documents.

## Current Architecture Posture

VentureOS is a Company Operating System, not an AI Operating System. AI is an execution mechanism, not the identity of the system.

VentureOS is capability-first, not agent-first. Agents are implementation details. The architecture hierarchy is:

Domain -> Capability -> Workflow -> Execution -> Implementation

The architecture is configured for Autonomy Level 1: Assisted Mode and must remain autonomy-ready.

## Technical Source Of Truth Map

- System layers: `docs/architecture/system-layers.md`
- System components: `docs/architecture/system-components.md`
- Event architecture: `docs/architecture/event-architecture.md`
- Database architecture: `docs/architecture/database-architecture.md`
- Runtime behavior: `docs/runtime/`
- Tool Gateway: `docs/architecture/tool-gateway.md`
- AI Gateway: `docs/architecture/ai-gateway.md`
- Execution Orchestrator: `docs/architecture/execution-orchestrator.md`
- Workflow Orchestrator compatibility note: `docs/architecture/workflow-orchestrator.md`
- Policy Engine: `docs/architecture/policy-engine.md`
- State machines: `docs/architecture/state-machines.md`
- Capability Registry: `docs/architecture/capability-registry.md` (primary)
- Agent Registry: `docs/architecture/agent-registry.md` (secondary)
- Agent evolution: `docs/architecture/agent-evolution.md`
- Founder Command Center: `docs/architecture/founder-command-center.md`
- Observability: `docs/architecture/observability.md`

## Architecture Rule

Technical implementation work must trace to this architecture index, an accepted ADR, and an active phase specification.

Implementation may be performed by an AI Agent, human, external API, internal service, or future execution engine.

## Next Architecture Task

Expand this document into the real Phase -1 architecture specification.
