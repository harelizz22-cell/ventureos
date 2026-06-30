# ADR-047: Debate, Consensus, And Dissent

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Debate, Consensus, and Dissent decision.

## Status

Accepted

## Context

Strategic review must preserve arguments, evidence, assumptions, confidence, disagreement, risk objections, and minority opinions. Consensus must summarize review without erasing material dissent.

## Decision

VentureOS adopts Debate Engine and Consensus Engine as first-class Strategic Review Domain architecture concepts.

Material dissent must be recorded.

## Alternatives considered

- Produce only a single recommendation summary.
- Treat consensus as majority vote.
- Omit minority opinions from final recommendations.

## Rationale

Recording debate and dissent improves decision quality, auditability, risk visibility, and Founder trust.

## Risks

- Dissent may be over-weighted or under-weighted.
- Consensus may hide unresolved questions.
- Review participants may cite weak evidence.

## Consequences

- Debate output must include arguments for, arguments against, evidence, assumptions, confidence, disagreements, unresolved questions, risk objections, and minority opinions.
- Consensus output must include recommendation, confidence, scores, evidence quality, Enterprise Value impact, capital required, dissent summary, and required approvals.

## Enforcement

Consensus Engine produces governed recommendations only and must not make final decisions.
