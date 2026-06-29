# Capital Allocation Engine

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Capital Allocation Engine architecture.

## Purpose

The Capital Allocation Engine optimizes where capital should be allocated across the entire portfolio.

## Responsibilities

- Thesis alignment review input
- Investment planning
- Budget allocation
- Budget reallocation
- Scaling decisions
- Budget reduction
- Opportunity comparison
- Capital efficiency
- Portfolio optimization
- Portfolio diversification analysis
- Return on capital analysis

## Portfolio Capital Management

The system must eventually answer:

- Where should the next dollar be invested?
- Which Venture should receive more budget?
- Which Venture should stop receiving investment?
- Which Venture should be exited?
- Which Venture should be acquired?
- Which Venture should be merged?
- Which Venture should be paused?

## Rule

The Capital Allocation Engine generates governed recommendations. It does not execute investments or move money.

No capital allocation may proceed without Thesis alignment review.

Capital allocation recommendations must consider Portfolio Diversification, expected ROI, risk, approval requirements, and expected Enterprise Value impact.

## Placeholder Status

This is an architecture placeholder. It does not define allocation formulas, investment execution, financial integrations, schemas, or implementation.
