# ADR-018: Opportunity Score

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Opportunity Score decision.

## Status

Accepted

## Context

Portfolio-first capital allocation requires comparable opportunity evaluation across internal ventures and future external investments.

## Decision

VentureOS adopts Opportunity Score as a first-class executive metric.

Opportunity Score combines market size, competition, execution complexity, founder confidence, evidence quality, expected revenue, expected profit, strategic alignment, risk, expected ROI, time to revenue, and capital required.

## Consequences

- Opportunity comparison becomes a first-class architectural concern.
- Capital Allocation Engine and Investment Engine may use Opportunity Score as input.
- Opportunity Score must remain evidence-aware and governance-aware.

## Enforcement

Opportunity Score must not execute investments, allocate capital, or override Founder approval.

