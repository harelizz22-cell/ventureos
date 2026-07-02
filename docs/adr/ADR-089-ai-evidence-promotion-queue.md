# ADR-089: AI Evidence Promotion Queue

Parent: `docs/architecture/ai-output-classification.md`

Status: Accepted

## Context

AI-generated Candidate Evidence needs governed promotion so it cannot be mistaken for Verified Evidence.

## Decision

Adopt a governed AI Evidence Promotion Queue with delegation rules, batch constraints, throughput visibility, backlog handling, denied promotion audit, deferred promotion audit, and an explicit rule that Candidate Evidence is never Verified Evidence.

## Alternatives

- Promote AI output directly.
- Require manual one-by-one review without queue visibility.
- Leave promotion queue behavior to implementation.

## Rationale

Promotion governance protects Evidence integrity and keeps AI output from polluting Evidence Ledger.

## Risks

Promotion backlog may delay decisions if not monitored.

## Consequences

AI Output Classification and Evidence Ledger must preserve queue status, reviewer authority, and audit outcomes.

## Enforcement

Evidence Ledger must not accept AI Candidate Evidence as Verified Evidence without approved promotion.
