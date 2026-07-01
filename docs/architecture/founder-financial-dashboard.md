# Founder Financial Dashboard

Parent: `docs/architecture/founder-command-center.md`

Source Of Truth: This file is the source of truth for Founder Financial Dashboard architecture.

## Purpose

Founder Financial Dashboard gives the Founder a clear, governed view of VentureOS financial state, capital decisions, risk, and upcoming funding actions.

The dashboard is visibility and decision support. It does not move money, approve capital, or bypass Policy Engine.

## Required Founder Visibility

Founder must always see:

- Cash available.
- Capital reserved.
- Capital committed.
- Capital released.
- Expected runway.
- Burn rate.
- Portfolio allocation.
- ROI.
- Enterprise Value trend.
- Investment pipeline.
- Financial risk score.
- Upcoming funding decisions.

## Decision Support

The dashboard must distinguish:

- Confirmed financial facts.
- Approved budgets.
- Reserved capital.
- Committed capital.
- Released capital.
- Spent capital.
- Verified spend.
- Recovered or cancelled capital.
- AI recommendations.
- Assumptions and forecasts.

## Governance Requirements

- High-value and policy-defined actions must be Founder-visible before approval.
- Dashboard actions must route through Policy Engine and Treasury Domain.
- Founder approvals must be recorded in Decision Ledger and Audit Ledger.
- No autonomous money movement is allowed.

## Security Requirements

- Dashboard visibility must respect Organization, Portfolio, Venture, role, and actor authorization.
- Financial state must be tamper-evident.
- Security alerts, emergency locks, and capital freezes must be visible.

## Audit Requirements

Dashboard must preserve:

- Who viewed or approved capital-sensitive actions where policy requires it.
- What financial state was shown at decision time.
- Which policy version or snapshot was evaluated.
- Which Evidence and Decision records supported the view.

## Placeholder Status

This is architecture documentation only. It does not define UI, APIs, schemas, payment systems, financial integrations, secrets, or implementation.
