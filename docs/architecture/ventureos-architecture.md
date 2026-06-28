# VentureOS Architecture

Parent: `docs/project/ventureos-system-bible.md`

Source Of Truth: This file is the technical architecture index for VentureOS.

## Purpose

This document identifies the source of truth for each technical architecture concern. It does not replace concern-specific architecture documents.

## Current Architecture Posture

VentureOS is a Company Operating System, not an AI Operating System. AI is an execution mechanism, not the identity of the system.

VentureOS is Portfolio-first and capability-first, not agent-first. A single venture is simply a portfolio containing one venture. Agents are implementation details.

The architecture hierarchy is:

Founder -> Organization -> Portfolio -> Venture -> Domain -> Capability -> Workflow -> Execution -> Evidence -> Decision -> Audit

The architecture is configured for Autonomy Level 1: Assisted Mode and must remain autonomy-ready.

The long-term architecture must support multiple Organizations, multiple Portfolios, hundreds of Ventures, thousands of Capabilities, and millions of Events without architectural redesign.

## Technical Source Of Truth Map

- Context map: `docs/architecture/context-map.md`
- Organization and Portfolio model: `docs/architecture/organization-portfolio-model.md`
- Domain model: `docs/architecture/domain-model.md`
- Knowledge Domain: `docs/architecture/knowledge-domain.md`
- Identity Domain: `docs/architecture/identity-domain.md`
- Resource Domain: `docs/architecture/resource-domain.md`
- System layers: `docs/architecture/system-layers.md`
- System components: `docs/architecture/system-components.md`
- Event architecture: `docs/architecture/event-architecture.md`
- Database architecture: `docs/architecture/database-architecture.md`
- Asset Registry: `docs/architecture/asset-registry.md`
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

Every future capability must be multi-venture aware and must identify its owning Domain.

## Next Architecture Task

Expand this document into the real Phase -1 architecture specification.
