# ADR-049: Enterprise Knowledge Graph

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Enterprise Knowledge Graph decision.

## Status

Accepted

## Context

Phase 2 Workstream 01B closes an architecture gap around long-term organizational knowledge, memory, and reasoning. VentureOS needs a governed relationship model that connects approved records without turning knowledge into an unstructured data dump.

## Decision

VentureOS adopts Enterprise Knowledge Graph as the structured relationship layer across approved knowledge, Evidence, Decisions, Ventures, Markets, outcomes, risks, and architecture entities.

Graph entries must distinguish facts, Evidence, Decisions, assumptions, forecasts, opinions, and learning.

## Alternatives considered

- Keep relationships implicit inside documents and future databases.
- Let Agents build temporary private knowledge graphs.
- Treat all retrieved knowledge as equivalent regardless of source, classification, or governance status.

## Rationale

A governed relationship layer strengthens long-term organizational intelligence, supports future reasoning, and preserves traceability to approved source records.

## Risks

- The graph may become an ungoverned data dump.
- Forecasts, opinions, or AI outputs may be mistaken for Evidence.
- Cross-venture graph traversal may bypass isolation if not policy-governed.

## Consequences

- Graph entries must trace back to approved source records.
- Graph classifications must be explicit.
- The graph supports reasoning and discovery but does not replace Evidence, Decisions, Audit, or source-of-truth records.

## Enforcement

No Enterprise Knowledge Graph entry may be accepted unless it has approved source provenance, scope, classification, and auditability.
