# ADR-056: AI Output Classification

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted AI Output Classification decision.

## Status

Accepted

## Context

AI outputs can assist VentureOS but may hallucinate, omit sources, or appear more authoritative than they are. Evidence Ledger integrity requires explicit classification and promotion governance.

## Decision

VentureOS adopts AI Output Classification with the lifecycle Draft -> Recommendation -> Candidate Evidence -> Verified Evidence.

AI output is never Evidence by default.

## Alternatives considered

- Store AI output directly as Evidence.
- Let each Agent decide output classification.
- Treat AI citations as automatic verification.

## Rationale

Explicit classification keeps AI useful without weakening Evidence, Decision, Audit, or Founder governance.

## Risks

- Promotion processes may add review overhead.
- Missing model, prompt, context, or source traceability may limit usefulness.
- Users may still over-trust AI-generated recommendations.

## Consequences

- AI output must cite sources, assumptions, confidence, uncertainty, and limitations where meaningful.
- Promotion to Evidence requires governance.
- AI hallucination risk must be explicitly mitigated.

## Enforcement

AI output must not enter Evidence Ledger as Verified Evidence without Evidence Promotion governance.
