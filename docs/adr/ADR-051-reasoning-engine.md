# ADR-051: Reasoning Engine

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Reasoning Engine decision.

## Status

Accepted

## Context

VentureOS needs a governed architecture component that can derive conclusions from approved knowledge, Organizational Memory, Evidence, and current context without replacing Founder authority, Evidence promotion, or Decision governance.

## Decision

VentureOS adopts Reasoning Engine as the explainable reasoning and recommendation component for approved knowledge, memory, Evidence, and context.

Reasoning Engine does not make final Decisions.

## Alternatives considered

- Let Agents reason privately without governed citations.
- Treat reasoning outputs as Evidence automatically.
- Merge reasoning into Learning Engine or Strategic Review Domain.

## Rationale

Explainable reasoning strengthens opportunity, risk, investment, strategy, portfolio, capital allocation, hypothesis, and Thesis review while preserving governance boundaries.

## Risks

- Reasoning outputs may be mistaken for verified Evidence.
- Recommendations may be mistaken for final Decisions.
- Missing citations may make reasoning unauditable.

## Consequences

- Reasoning outputs must cite source knowledge, Evidence records, assumptions, confidence, uncertainty, and dissent where relevant.
- Reasoning outputs may become Candidate Evidence only through AI Output Classification and Evidence Promotion governance.
- Founder or approved governance policy remains final authority.

## Enforcement

No reasoning output may be used for governed review unless it cites source knowledge, Evidence records, assumptions, confidence, uncertainty, and dissent where relevant.
