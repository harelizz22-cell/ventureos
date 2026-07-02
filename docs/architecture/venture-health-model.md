# Venture Health Model

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Venture Health architecture.

## Purpose

The Venture Health Model defines how each Venture expresses current operating health across multiple dimensions.

## Minimum Health Dimensions

- Revenue Health
- Execution Health
- Governance Health
- Evidence Health
- Growth Health
- Infrastructure Health
- Operational Health
- Founder Confidence
- Activity Health
- Termination Risk

## Rules

- Every Venture owns multiple health dimensions.
- Each score has its own calculation model.
- Overall Venture Health is derived from the dimensions.
- Health must be visible in the Founder Operating Console.
- Venture Health must detect dormant, inactive, abandoned, and de facto termination risk.
- De facto termination detection must trigger archive review and mandatory learning extraction.

## De Facto Termination Signals

Venture Health may mark a Venture as:

- Dormant: no meaningful progress within the expected activity window.
- Inactive: no active execution, validation, revenue, operational, or governance activity within the policy-defined window.
- Abandoned: no owner action, no active plan, and no current governance path.

These states do not delete the Venture. They trigger review, audit, and learning extraction.

## Placeholder Status

This is an architecture placeholder. It does not define scoring formulas, thresholds, UI, schema, or implementation.
