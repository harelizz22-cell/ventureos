# ADR-092: Dissent Preservation

Parent: `docs/architecture/strategic-review-domain.md`

Status: Accepted

## Context

Strategic Review can lose important minority concerns if consensus summaries flatten dissent.

## Decision

Require minority opinion, strongest counter-argument, dissent confidence, Founder override linkage, and dissent preservation in Investment Memo.

## Alternatives

- Record only final consensus.
- Record dissent only when Founder asks.
- Store dissent outside the memo.

## Rationale

Founder decisions are stronger when material dissent remains visible and auditable.

## Risks

Review artifacts may become longer.

## Consequences

Debate Engine, Consensus Engine, Strategic Review Domain, and Investment Memo Generator must preserve dissent.

## Enforcement

Investment Memo must include minority opinion or state no material dissent was identified, and must preserve strongest counter-argument.
