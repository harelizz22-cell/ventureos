# Capital Stress Simulator

Parent: `docs/architecture/treasury-domain.md`

Source Of Truth: This file is the source of truth for Capital Stress Simulator architecture.

## Purpose

Capital Stress Simulator evaluates adverse financial scenarios before major capital commitments, releases, portfolio changes, or funding plans.

## Simulated Scenarios

### Market Crash

Models lower revenue, lower valuations, delayed fundraising, higher cost of capital, and reduced exit optionality.

### Venture Failure

Models full or partial Venture failure, sunk cost, recovery options, asset recovery, and portfolio impact.

### Double Budget

Models the effect of a Venture or initiative requiring twice the approved capital.

### Zero Revenue

Models delayed monetization, no revenue, or revenue collapse against runway and follow-on requirements.

### Delayed Launch

Models launch delay impact on burn, opportunity cost, milestone funding, and runway.

### Fundraising Failure

Models failure to secure expected external capital or follow-on funding.

### Multiple Simultaneous Failures

Models correlated failure across Ventures, markets, providers, revenue channels, or operating dependencies.

## Required Outputs

- Recommended actions.
- Capital preservation strategy.
- Confidence.
- Remaining runway.
- Key assumptions.
- Material uncertainties.
- Founder-visible warnings.

## Governance Rules

- Simulation output informs recommendations and approvals; it does not move money.
- Simulation output is not Evidence until promoted through governed Evidence processes.
- Major capital allocation or release may require a fresh stress simulation when policy requires it.

## Placeholder Status

This is architecture documentation only. It does not define simulation models, formulas, external data feeds, financial integrations, schemas, secrets, or implementation.
