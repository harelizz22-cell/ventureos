# ADR-037: AI Output Classification

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted AI Output Classification decision.

## Status

Accepted

## Context

AI output can be useful for drafting, recommendations, and candidate evidence, but unreviewed AI output must not enter the Evidence Ledger as verified evidence.

## Decision

VentureOS adopts the AI output lifecycle:

Draft -> Recommendation -> Candidate Evidence -> Verified Evidence

AI output must never enter Evidence Ledger directly without promotion governance.

## Consequences

- Evidence Ledger integrity is protected from unverified AI output.
- Promotion governance becomes required before AI-supported content becomes Evidence.
- Audit must preserve the classification and promotion path.

## Enforcement

AI output cannot be treated as Verified Evidence until source review, confidence assessment, evidence quality evaluation, and required approval are complete.
