# Portfolio Governance

Parent: `docs/architecture/treasury-domain.md`

Source Of Truth: This file is the source of truth for Portfolio Governance architecture.

## Purpose

Portfolio Governance protects long-term Enterprise Value by managing capital concentration, exposure, risk balance, liquidity, expected return, and follow-on planning across the portfolio.

## Portfolio Diversification

Portfolio Governance uses Portfolio Diversification to avoid over-concentration across sectors, geographies, stages, technologies, capital, AI providers, revenue models, and correlated risks.

## Sector Exposure

Sector exposure tracks concentration by market sector.

Rules:

- Sector limits must be policy-visible.
- Overexposure requires review before additional allocation.

## Capital Concentration

Capital concentration tracks how much capital is allocated or reserved for a Venture, sector, stage, provider, technology, geography, or revenue model.

Rules:

- Concentration must include Available, Reserved, Committed, Approved, Released, and Spent capital where relevant.
- No concentration analysis may count the same capital twice.

## Risk Balancing

Risk balancing compares high-risk, medium-risk, and low-risk allocations against Thesis, runway, expected return, and Enterprise Value impact.

Rules:

- Risk balancing informs recommendations but does not override Founder approval.
- Material correlated risk requires governed review.

## Liquidity Planning

Liquidity planning ensures VentureOS can meet approved obligations, preserve runway, and avoid overcommit.

Rules:

- Liquidity planning must include follow-on reserves and milestone commitments.
- Liquidity risk must be visible before major capital allocation.

## Expected Return

Expected return estimates must be linked to assumptions, Evidence, confidence, and time horizon.

Rules:

- Expected return must not use guaranteed return language.
- Expected return is an input to governance, not autonomous approval.

## Portfolio Health

Portfolio health combines financial state, venture outcomes, risk, runway, diversification, expected return, and Enterprise Value trend.

Rules:

- Health indicators must distinguish confirmed facts, estimates, assumptions, and AI-generated recommendations.

## Follow-On Planning

Follow-on planning identifies future funding needs and preserves capital discipline across existing and future Ventures.

Rules:

- Follow-on plans must be explicit.
- Follow-on plans must be evaluated against capital lifecycle, treasury risk, stress simulations, and Founder constraints.

## Placeholder Status

This is architecture documentation only. It does not define investment formulas, securities activity, legal structures, fund administration, schemas, integrations, or implementation.
