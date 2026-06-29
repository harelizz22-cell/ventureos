# ADR-030: Funding Engine

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Funding Engine decision.

## Status

Accepted

## Context

VentureOS needs future architecture for planning funding rounds, capital targets, milestone-based funding, funding readiness, and budget release recommendations without authorizing regulated financial workflows.

## Decision

VentureOS adopts the Funding Engine as a future first-class architecture concept.

Funding Engine may recommend funding actions, but must not execute regulated financial activity without approved legal/compliance framework.

## Alternatives Considered

- Keep funding planning outside VentureOS.
- Treat funding plans as simple budget notes.
- Add funding execution behavior before legal/compliance boundaries.

## Rationale

Funding planning affects Enterprise Value, capital allocation, Investment Readiness, milestone execution, risk, and Founder decisions. It needs architecture before implementation, while preserving a hard compliance boundary.

## Risks

- Funding recommendations may be confused with fundraising execution.
- Capital commitment tracking may be mistaken for custody or securities processing.
- Funding failure handling may require legal or investor communication review.

## Compliance Notes

The Funding Engine does not authorize VentureOS to raise funds, sell securities, hold investor money, process payments, or execute investments.

Legal/compliance structure must be approved before regulated activity.

## Consequences

- Funding round planning and capital target definition become architecture concerns.
- Milestone-based capital release and funding readiness become connected concerns.
- Funding recommendations remain governed and compliance-gated.

## Enforcement

Funding Engine may recommend. It must not move money, execute securities transactions, or bypass Founder governance, Policy Engine, Evidence, Decision, Audit, or legal/compliance review.
