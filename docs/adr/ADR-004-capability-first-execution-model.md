# ADR-004: Capability-First Execution Model

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted capability-first execution model decision.

## Status

Accepted

## Context

VentureOS must preserve its identity as a company operating system. AI can support execution, but the system identity cannot become agent-centric or AI-centric. Previous documentation included Workflow Orchestrator terminology and agent references that could be interpreted as agent-first execution ownership.

The architecture requires a clear hierarchy that separates business domains, capabilities, workflows, execution, and implementation mechanisms.

## Decision

VentureOS is a Company Operating System, not an AI Operating System. AI is an execution mechanism, not the identity of the system.

VentureOS is capability-first, not agent-first. Agents are implementation details.

The architecture hierarchy is:

Domain -> Capability -> Workflow -> Execution -> Implementation

Implementation may be:

- AI Agent.
- Human.
- External API.
- Internal service.
- Future execution engine.

Workflow Orchestrator terminology is replaced by Execution Orchestrator terminology. The Execution Orchestrator owns execution flow.

The CEO Agent may advise, summarize, coordinate recommendations, and request decisions. The CEO Agent must not orchestrate the system or own execution flow.

A development-time Decision Guardian is added to ensure agreed decisions are documented before implementation proceeds.

## Alternatives Considered

- Agent-first architecture: rejected because it makes agents the primary model instead of capabilities.
- AI Operating System identity: rejected because VentureOS is a company operating system that may use AI, humans, APIs, services, or future engines.
- CEO Agent as orchestrator: rejected because execution ownership must be system-level, governed, and independent of any single agent.
- Keeping Workflow Orchestrator as the primary term: rejected because it is too narrow for capability invocation, approvals, failures, recovery, and mixed execution mechanisms.

## Reason

Capability-first architecture keeps VentureOS stable as implementation mechanisms change. It prevents agent proliferation from becoming architecture, keeps governance attached to capabilities and execution, and preserves founder control.

## Risks

- Existing documents may retain old terminology.
- Future contributors may treat agents as the primary architecture unit.
- Execution Orchestrator responsibilities may need deeper Phase -1 specification.
- Compatibility terminology may confuse readers until older references are fully migrated.

## Consequences

- Capability Registry is primary.
- Agent Registry is secondary.
- Execution Orchestrator owns execution flow.
- Workflow Orchestrator becomes compatibility terminology.
- CEO Agent cannot orchestrate the system.
- Implementation decisions must not assume AI agent execution by default.
- Development-time Decision Guardian must block undocumented decision drift.

## Enforcement Rules

- No Agent-first language may be used as the primary architecture model.
- CEO Agent must not be described as system orchestrator.
- Execution Orchestrator must be documented as owner of execution flow.
- Capability Registry must be treated as primary.
- Agent Registry must be treated as secondary.
- Architecture-changing decisions require ADR review.
- Codex must not implement from conversation-only decisions.

