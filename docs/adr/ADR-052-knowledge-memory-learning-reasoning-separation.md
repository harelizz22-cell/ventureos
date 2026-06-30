# ADR-052: Knowledge, Memory, Learning, And Reasoning Separation

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted separation of Knowledge Domain, Enterprise Knowledge Graph, Organizational Memory, Learning Engine, and Reasoning Engine.

## Status

Accepted

## Context

Phase 2 Workstream 01B adds long-term knowledge, memory, and reasoning architecture. These concerns are related but must not collapse into one ambiguous component.

## Decision

VentureOS keeps these concerns separate:

- Knowledge Domain owns knowledge assets and retrieval capabilities.
- Enterprise Knowledge Graph answers how facts, Evidence, Decisions, Ventures, Markets, and outcomes are connected.
- Organizational Memory answers what happened and what the organization remembers.
- Learning Engine answers what was learned from outcomes.
- Reasoning Engine answers what can be inferred from what VentureOS knows.

## Alternatives considered

- Merge all concerns into Learning Engine.
- Treat Knowledge Domain as responsible for every knowledge, memory, and reasoning behavior.
- Let future implementation decide boundaries later.

## Rationale

Separation preserves source-of-truth clarity, auditability, governance, and future implementation flexibility.

## Risks

- Documents may duplicate responsibility across these components.
- Future implementation may blur boundaries.
- Reasoning or learning may rewrite memory or source records if governance is weak.

## Consequences

- Each concern has a distinct source-of-truth document.
- Learning Engine remains separate.
- Knowledge Domain remains separate.
- No new strategic concepts should be added until Phase 2 is completed and reviewed.

## Enforcement

Future documents and implementations must not merge Knowledge Domain, Enterprise Knowledge Graph, Organizational Memory, Learning Engine, and Reasoning Engine responsibilities without a new accepted ADR.
