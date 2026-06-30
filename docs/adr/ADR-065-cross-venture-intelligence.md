# ADR-065: Cross-Venture Intelligence

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Cross-Venture Intelligence decision.

## Status

Accepted

## Context

VentureOS needs portfolio-wide intelligence without breaking Venture isolation or leaking raw Venture data between Ventures.

## Decision

VentureOS adopts Cross-Venture Intelligence for aggregate analytics, portfolio KPIs, trend detection, pattern recognition, governed cross-Venture reasoning, Evidence aggregation, benchmarking, and shared learning.

## Alternatives

- Block all cross-Venture intelligence.
- Permit unrestricted cross-Venture data access.
- Rely on Business Intelligence without explicit isolation rules.

## Rationale

Portfolio-level intelligence is necessary for Enterprise Value while governed isolation preserves trust, auditability, and tenant safety.

## Risks

- Aggregates may leak sensitive raw data.
- Reasoning may blur evidence boundaries.
- Shared learning may overgeneralize across Ventures.

## Consequences

- Raw Venture data must remain isolated unless policy explicitly allows access.
- Cross-Venture reasoning is governed and recommendation-only.
- Aggregate outputs must preserve scope, source, and auditability.

## Enforcement

Raw Venture data must not leak between Ventures unless Policy Engine explicitly allows it.
