# Investment Engine

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Investment Engine architecture.

## Purpose

The Investment Engine evaluates external and internal investment opportunities.

## Responsibilities

- Thesis alignment review input
- Opportunity scoring
- Portfolio diversification analysis
- Risk evaluation
- Expected ROI
- Capital recommendation
- Investment readiness input
- Investment dossier input
- Investor marketplace readiness input
- Stage gate decisions
- Exit recommendations
- Portfolio diversification
- Investment history
- Investment lifecycle
- Investment governance

## External Investment Support

Future architecture must support evaluating investments in external startups.

The system may:

- Discover opportunities
- Analyze opportunities
- Score opportunities
- Compare opportunities
- Recommend investments
- Track investments
- Recommend exits

The system must not autonomously transfer money or execute investments.

Financial execution always requires Founder-defined governance.

Future investor marketplace participation requires Investment Readiness review, Investment Dossier preparation, legal/compliance gating, and Founder approval.

Major investment and capital recommendations should use Strategic Review Domain, Dynamic Review Council, Debate Engine, Consensus Engine, and Investment Memo Generator where required by policy.

## Rule

The Investment Engine generates governed recommendations. It never executes investments.

No external investment, acquisition, or capital allocation recommendation may proceed without Thesis alignment review.

Investment recommendations must consider Portfolio Diversification where meaningful.

The Investment Engine must not claim VentureOS can legally raise funds, sell securities, hold investor money, or execute investments without approved legal/compliance structure.

## Placeholder Status

This is an architecture placeholder. It does not define financial integrations, investment transactions, external data integrations, schemas, or implementation.
