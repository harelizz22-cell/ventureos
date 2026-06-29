# ADR-032: Investment Dossier

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Investment Dossier decision.

## Status

Accepted

## Context

Future investor-facing opportunities require a structured explanation package that distinguishes assumptions, evidence, forecasts, confirmed facts, risks, capital needs, governance, and compliance status.

## Decision

VentureOS adopts Investment Dossier as a future first-class architecture concept.

Investment Dossiers must clearly distinguish assumptions, evidence, forecasts, and confirmed facts.

## Alternatives Considered

- Use free-form investor summaries.
- Use Opportunity Score as the investor-facing package.
- Delay dossier architecture until marketplace implementation.

## Rationale

Investor-facing explanation must be structured, evidence-based, reviewable, and compliance-aware. A dossier prevents uncontrolled narrative drift and supports legal/compliance review.

## Risks

- Forecasts may be mistaken for facts.
- Expected ROI range may be mistaken for guaranteed return.
- Dossiers may be shared before legal/compliance review.

## Compliance Notes

No guaranteed return language is allowed.

The dossier does not sell securities, process investments, approve investors, or authorize capital movement.

## Consequences

- Investor-facing materials require a structured package.
- Evidence summary, risk summary, legal/compliance status, and suitability notes become required.
- Investment Marketplace depends on approved dossiers.

## Enforcement

No Investment Dossier may be used for investor exposure until Investment Readiness, Founder approval, and legal/compliance gating are satisfied.
