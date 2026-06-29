# ADR-026: Portfolio Diversification

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Portfolio Diversification decision.

## Status

Accepted

## Context

Architecture Audit #006 requires VentureOS to avoid over-concentration across sectors, geographies, stages, technologies, capital, AI providers, revenue models, and correlated risks.

## Decision

VentureOS adopts Portfolio Diversification as a first-class architecture concept.

Portfolio Diversification must inform capital allocation, investment recommendations, acquisition recommendations, Venture scaling recommendations, and Enterprise Value evaluation.

## Consequences

- Concentration risk becomes visible before major strategic or capital decisions.
- Business Intelligence, Capital Allocation, Investment, and Enterprise Value analysis must support diversification awareness.
- Diversification analysis remains recommendation-only unless future approved governance defines execution behavior.

## Enforcement

Portfolio Diversification supports governed recommendations. It does not execute investments, move money, or override Founder approval.
