# ADR-016: Capital Allocation Engine

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Capital Allocation Engine decision.

## Status

Accepted

## Context

Portfolio-first architecture requires governed decisions about where capital should be allocated across Ventures and opportunities.

## Decision

VentureOS adopts the Capital Allocation Engine to optimize where capital should be allocated across the entire portfolio.

## Consequences

- Capital allocation becomes a first-class architecture concern.
- Capital efficiency, return on capital, scaling decisions, budget reductions, and portfolio optimization become governed concepts.
- The system may recommend capital movement but must not execute investments autonomously.

## Enforcement

Capital allocation recommendations must include evidence, expected ROI, risk, expected Enterprise Value impact, and approval requirements.

