# Treasury Risk Engine

Parent: `docs/architecture/treasury-domain.md`

Source Of Truth: This file is the source of truth for Treasury Risk Engine architecture.

## Purpose

Treasury Risk Engine evaluates financial risk across cash, runway, concentration, depletion, dependency, downturn, cost growth, and budget overrun scenarios before capital-sensitive Decisions.

## Cash Runway

Cash runway estimates how long available and reserved capital can support approved operations.

Requirements:

- Distinguish Available, Reserved, Committed, Approved, Released, Spent, and Recovered capital.
- Show assumptions, burn rate, confidence, and data freshness.

## Concentration Risk

Concentration risk identifies excessive exposure by Venture, sector, geography, stage, technology, AI provider, revenue model, or correlated risk factor.

## Capital Depletion

Capital depletion evaluates whether approved and projected commitments will exhaust capital below policy-defined thresholds.

## Funding Dependency

Funding dependency evaluates exposure to future fundraising, expected revenue, follow-on capital, customer receipts, grants, debt, or investor commitments.

## Market Downturn Simulation

Market downturn simulation evaluates the effect of reduced revenue, longer sales cycles, delayed fundraising, lower valuations, and higher cost of capital.

## Unexpected Cost Growth

Unexpected cost growth evaluates how vendor increases, infrastructure usage, staffing, compliance, legal, marketing, AI provider costs, or operational expenses affect runway.

## Budget Overruns

Budget overrun evaluation compares actual or projected spend against approved budgets, milestone funding plans, and holdbacks.

## Outputs

- Risk score.
- Risk explanation.
- Recommended mitigation.
- Required review.
- Founder visibility flag.
- Policy Engine escalation trigger.

## Governance Rules

- Risk outputs are recommendations or signals, not final Decisions.
- High-risk capital actions require governed review.
- Capital-sensitive execution must fail closed when Treasury Risk Engine cannot evaluate required risk inputs.

## Placeholder Status

This is architecture documentation only. It does not define risk formulas, models, data pipelines, external financial integrations, schemas, secrets, or implementation.
