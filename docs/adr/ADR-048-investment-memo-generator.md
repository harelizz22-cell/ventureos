# ADR-048: Investment Memo Generator

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Investment Memo Generator decision.

## Status

Accepted

## Context

Major capital decisions require a formal internal review artifact. Professional venture capital investment committee memo structures provide useful architectural inspiration when adapted to VentureOS governance.

## Decision

VentureOS adopts Investment Memo Generator as a Strategic Review Domain architecture concept.

Investment Memo becomes the formal internal review artifact before major capital decisions.

## Alternatives considered

- Use free-form recommendation summaries.
- Use investor-facing dossiers for internal decisions.
- Skip formal memo structure until implementation.

## Rationale

Investment Memos preserve opportunity summary, evidence, due diligence, feasibility, financial model, expected ROI, Enterprise Value impact, use of funds, milestones, risk, dissent, legal/compliance review, recommendation, and approvals.

## Risks

- Memo may be mistaken for a legal offering document.
- Weak evidence may be presented too confidently.
- Dissent may be omitted if memo generation is not governed.

## Consequences

- Major capital decisions require a formal governed review artifact.
- Investment Memo is internal unless future compliance explicitly permits investor-facing use.
- Dissent and legal/compliance review must be included.

## Enforcement

Investment Memo is not a legal offering document and does not authorize investment execution, fundraising, capital movement, or Founder approval bypass.
