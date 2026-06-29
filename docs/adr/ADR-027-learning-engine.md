# ADR-027: Learning Engine

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Learning Engine decision.

## Status

Accepted

## Context

Architecture Audit #006 requires VentureOS to convert outcomes into reusable knowledge so future recommendations improve without relying on undocumented memory or mutable current-state assumptions.

## Decision

VentureOS adopts the Learning Engine as a first-class architecture concept.

Learning updates must be evidence-backed and auditable.

## Consequences

- Outcomes from ventures, opportunities, investments, founder overrides, budget decisions, pricing experiments, and acquisitions become learning inputs.
- Learning can recommend changes to Knowledge, Thesis, Opportunity Score assumptions, capital allocation assumptions, and strategic constraints.
- Historical Evidence, Decisions, and Audit records remain immutable.

## Enforcement

Learning Engine may recommend updates. It does not silently rewrite source-of-truth records, override Founder approval, or bypass governance.
