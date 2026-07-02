# ADR-098: Reasoning-To-Evidence Enforcement

Parent: `docs/contracts/evidence-ledger-spec.md`

Status: Accepted

## Context

Reasoning outputs may influence decisions, but they must not enter Evidence Ledger directly.

## Decision

Evidence Ledger must reject direct Reasoning outputs. Reasoning output requires source classification, promotion record, and promotion path before Evidence write.

## Alternatives

- Allow Reasoning outputs to be written as Evidence.
- Require reviewer judgment without runtime enforcement.
- Treat all reasoning as Candidate Evidence automatically.

## Rationale

Reasoning and Evidence are separate concerns. Promotion protects Evidence integrity.

## Risks

Promotion steps may slow decision workflows.

## Consequences

Reasoning Engine, AI Output Classification, and Evidence Ledger must enforce the promotion path.

## Enforcement

Evidence Ledger writes fail closed when source classification or promotion record is missing.
