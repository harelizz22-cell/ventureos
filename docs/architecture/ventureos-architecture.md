# VentureOS Architecture

Parent: `docs/project/ventureos-system-bible.md`

Source Of Truth: This file is the technical architecture index for VentureOS.

## Purpose

This document identifies the source of truth for each technical architecture concern. It does not replace concern-specific architecture documents.

## Official Definitions

These definitions are architectural vocabulary. All future documents must use them consistently.

- Capability: A durable system ability owned by a Domain and invokable through governed execution. A Capability is independent of any specific implementation mechanism.
- Domain: A business area that owns Capabilities, Policies, Events, Workflows, Data, Interfaces, and future implementations.
- Workflow: A structured sequence of steps that coordinates a Capability or related Capabilities toward an outcome.
- Execution: A governed runtime attempt to perform a Workflow or invoke a Capability through an implementation mechanism.
- Evidence: Recorded support, proof, observation, source material, or validation input used before Decisions.
- Decision: A recorded choice made by an authorized actor based on Evidence and applicable governance.
- Audit: Append-only record of meaningful actions, state changes, approvals, denials, executions, events, and governance-relevant history.
- Event: A meaningful runtime fact emitted by VentureOS for auditability, coordination, observability, and decoupled subscription.
- Autonomy Level: A configured runtime permission level that defines what the system may observe, recommend, request, or execute.
- Execution Orchestrator: The architecture component that owns execution flow, capability invocation, governance enforcement, approval waiting, retries, timeouts, failure containment, event coordination, recovery triggering, and execution state tracking.

## Current Architecture Posture

VentureOS is a Company Operating System, not an AI Operating System. AI is an execution mechanism, not the identity of the system.

VentureOS is Portfolio-first and capability-first, not agent-first. A single venture is simply a portfolio containing one venture. Agents are implementation details.

The architecture hierarchy is:

Founder -> Organization -> Portfolio -> Venture -> Domain -> Capability -> Workflow -> Execution -> Evidence -> Decision -> Audit

Authority hierarchy:

Founder -> Organization -> Portfolio -> Venture

Business hierarchy begins at Organization. Founder remains the highest authority but is not a business entity.

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
- Cost Governance: `docs/governance/cost-governance.md`
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

All execution paths must pass through the Policy Engine. No Capability, Agent, Workflow, Tool, Service, or External Provider may self-approve execution.

If the Policy Engine is unavailable, VentureOS must fail closed. No execution is permitted while governance is unavailable.

Evidence Ledger, Decision Ledger, and Audit Ledger are three separate architectural concerns. Evidence must exist before Decision. Decision without Evidence is invalid. Audit is append-only. Audit entries cannot be edited. Evidence never changes historical Decision records.
