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

## Rule

The Investment Engine generates governed recommendations. It never executes investments.

No external investment, acquisition, or capital allocation recommendation may proceed without Thesis alignment review.

Investment recommendations must consider Portfolio Diversification where meaningful.

## Placeholder Status

This is an architecture placeholder. It does not define financial integrations, investment transactions, external data integrations, schemas, or implementation.
