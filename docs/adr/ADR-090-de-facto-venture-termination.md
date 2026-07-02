# ADR-090: De Facto Venture Termination

Parent: `docs/architecture/financial-feedback-loop.md`

Status: Accepted

## Context

Ventures may stop operating without a formal shutdown decision, risking lost learning and unclear lifecycle state.

## Decision

Adopt dormant, inactive, abandoned, and de facto termination detection with archive review trigger, mandatory learning extraction, and informal termination audit records.

## Alternatives

- Require only formal Venture closure.
- Let inactive Ventures remain unclassified.
- Handle informal termination only in project management.

## Rationale

Every Venture outcome must produce organizational learning, even when termination is informal.

## Risks

False positives may trigger archive review too early.

## Consequences

Venture Timeline, Venture Health Model, Learning Engine, and Financial Feedback Loop must support de facto termination signals.

## Enforcement

No dormant, inactive, abandoned, or informally terminated Venture may close archival review without learning extraction status and audit record.
