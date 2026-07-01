# Capital Allocation Governance

Parent: `docs/architecture/treasury-domain.md`

Source Of Truth: This file is the source of truth for Capital Allocation Governance architecture.

## Purpose

Capital Allocation Governance ensures capital is allocated with discipline, exposure awareness, auditability, and Founder-preserved control.

Capital Allocation Engine may recommend. Treasury may reserve, release, and track. Policy Engine governs. Founder retains final governance for capital-sensitive decisions.

## Allocation Limits

Allocation limits define maximum capital exposure by Organization, Portfolio, Venture, stage, sector, geography, risk class, technology dependency, AI provider, revenue model, and time horizon.

Rules:

- Limits must be policy-defined and auditable.
- Limit breaches require governed exception review.
- High-value exceptions require Founder approval.

## Capital Reservation

Capital reservation protects approved or pending allocations from being double-counted without moving money.

Rules:

- A reservation must have amount, scope, purpose, expiry, owner, linked request, and policy result.
- No capital can be allocated twice.
- Expired reservations must return to Available or enter governed review.
- Reservation conflicts must be visible to Treasury and Founder Financial Dashboard.

## Follow-On Reserves

Follow-on reserves preserve future funding capacity for ventures or investments that may need additional capital.

Rules:

- Follow-on reserves must be explicit and not hidden inside available capital.
- Follow-on reserves must include trigger conditions and expiry or review date.
- Follow-on reserves must be evaluated against portfolio exposure and runway.

## Portfolio Exposure

Capital allocation must consider exposure across sectors, geographies, stages, technologies, providers, revenue models, and correlated risks.

Rules:

- Portfolio Governance and Portfolio Diversification must inform major allocation decisions.
- Exposure exceptions require evidence and approval.

## Maximum Allocation Per Venture

Each Venture must have a maximum allocation boundary defined by stage, risk, expected return, strategic fit, available capital, and Founder policy.

Rules:

- Maximum allocation may change only through governed approval.
- A Venture cannot consume capital in ways that bypass its approved allocation envelope.

## Capital Conflict Resolution

Capital conflicts occur when multiple requests compete for the same available capital, exceed exposure limits, or create inconsistent reservations.

Rules:

- Conflicts must be detected before approval or release.
- Conflict resolution must consider Enterprise Value impact, Thesis alignment, evidence quality, risk, liquidity, runway, and Founder constraints.
- Treasury resolves state integrity; it does not decide business priority.

## Dynamic Reallocation

Dynamic reallocation moves capital priority between approved or reserved uses when evidence, risk, runway, or strategic constraints change.

Rules:

- Reallocation requires Policy Engine review.
- Reallocation must preserve the original audit record and create a new Decision record.
- Released or spent capital cannot be silently reallocated.

## Emergency Freeze

Emergency freeze prevents further capital action when security, fraud, policy, liquidity, compliance, or ledger integrity risk is detected.

Rules:

- Emergency freeze must fail closed.
- Emergency freeze must be Founder-visible.
- Release from freeze requires governed review and audit.

## Capital Recovery

Capital recovery governs unused capital, refunds, clawbacks, cancelled funding, or recovered spend.

Rules:

- Recovery must reference the original lifecycle record.
- Recovered capital must enter Available, Reserved, or Closed through a governed lifecycle transition.
- Recovery evidence is required.

## Placeholder Status

This is architecture documentation only. It does not define allocation formulas, investment execution, fund custody, financial integrations, schemas, secrets, or implementation.
