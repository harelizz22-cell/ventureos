# Organizational Memory

Parent: `docs/architecture/knowledge-domain.md`

Source Of Truth: This file is the source of truth for Organizational Memory architecture.

## Purpose

Organizational Memory is the historical memory layer of VentureOS.

It preserves what the organization has learned and experienced over time so knowledge does not stay trapped inside Agents, individual Ventures, or temporary execution context.

## Includes

Organizational Memory preserves durable history about:

- Past ventures
- Failed ventures
- Successful ventures
- Killed opportunities
- Investment decisions
- Founder overrides
- Customer interviews
- Pricing experiments
- Marketing experiments
- Product experiments
- Budget decisions
- Investor feedback
- Market research
- Operational incidents
- Recovery events
- Exits
- Acquisitions
- Lessons learned
- Playbooks

## Memory Requirements

Organizational Memory must be:

- Durable
- Scoped
- Auditable
- Reusable
- Linked to source records
- Separate from temporary execution context
- Separate from Agent memory
- Governed by Evidence, Decision, Audit, and Policy rules where relevant

## Scope Requirements

Memory records must preserve meaningful scope:

- `organization_id`
- `portfolio_id`
- `venture_id`
- Domain
- Capability
- Workflow
- Execution
- Actor
- Time
- Related Evidence
- Related Decision
- Related Audit

No global default Venture scope is allowed.

## Relationship To Other Components

- Knowledge Domain owns knowledge assets and retrieval capabilities.
- Organizational Memory preserves durable history.
- Enterprise Knowledge Graph connects memory records to related facts, Evidence, Decisions, Ventures, Markets, risks, and outcomes.
- Learning Engine answers what was learned from outcomes.
- Reasoning Engine uses approved memory as input for explainable reasoning outputs.

## VC Pattern Recognition Readiness

VentureOS should learn from professional venture capital pattern recognition as architecture readiness only.

Organizational Memory should eventually preserve enough historical context to detect:

- Repeated market patterns
- Repeated pricing failures
- Repeated customer acquisition cost failures
- Repeated Founder override outcomes
- Repeated Thesis violations
- Repeated successful GTM patterns
- Repeated regulatory blockers
- Repeated capital inefficiency patterns
- Repeated execution failure modes
- Repeatable playbooks

This is not active implementation. It does not define storage, agent memory, retrieval models, automation, or runtime services.

## Rule

Knowledge must not stay trapped inside Agents, individual Ventures, or temporary execution context.

Organizational Memory must be durable, scoped, auditable, and reusable.

## Placeholder Status

This is architecture documentation only. It does not define databases, schemas, embeddings, services, integrations, retention automation, UI, or implementation.
