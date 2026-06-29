# Domain Model

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for VentureOS business domains.

## Purpose

Define the Domain-first business model.

## Initial Domains

- Research
- Validation
- Build
- Marketing
- Sales
- Finance
- Operations
- Legal
- Governance
- Business Intelligence
- Knowledge
- Identity
- Resources
- Analytics

## Domain Ownership

Every Domain owns:

- Capabilities
- Policies
- Events
- Workflows
- Data
- Interfaces
- Future implementations

## Domain Declaration Standard

Every Domain must have an accepted Domain Declaration before it may be added to the Context Map.

A Domain Declaration must define:

- Name
- Purpose
- Owned data
- Exposed Capabilities
- Published Events
- Subscribed Events
- Domain-specific Policies
- Interfaces
- Owner
- Related ADRs

## Inter-Domain Communication

Domains never share state directly.

Allowed interaction channels are:

- Governed Capability invocation through the Execution Orchestrator and Policy Engine.
- Published Events through Event Architecture.

No Domain may read or write another Domain's database, tables, or in-memory state directly.

## Venture Scope Rule

Every Capability invocation, Execution, Evidence record, Decision record, Audit record, Event, Tool call, AI call, Asset, Cost record, and Investment recommendation must carry explicit scope:

- `organization_id`
- `portfolio_id`
- `venture_id`

No global default Venture scope is allowed.

## Capability Ownership Rule

Every Capability has exactly one owning Domain.

Co-owned Capabilities are not allowed. If multiple Domains are involved, the work must be split into multiple Capabilities coordinated by a Workflow or the Execution Orchestrator.

## Versioned Interface Rule

Domain interfaces, Capability contracts, and Event payloads must be versioned.

Breaking changes require:

- New version.
- Migration plan.
- ADR if architecturally significant.
- Compatibility window where required.

## Rule

Capabilities must belong to a Domain. Implementations do not define Domains.

Every Domain must be able to connect its Capabilities, Policies, Events, Workflows, Data, Interfaces, and future implementations to measurable business outcomes where meaningful.
