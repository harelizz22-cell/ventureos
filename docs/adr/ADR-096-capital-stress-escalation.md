# ADR-096: Capital Stress Escalation

Parent: `docs/architecture/capital-stress-simulator.md`

Status: Accepted

## Context

Capital stress outputs need escalation thresholds so severe financial risk is not treated as optional advice.

## Decision

Adopt capital stress severity levels, mandatory Founder review threshold, mandatory Treasury review threshold, emergency freeze threshold, and optional recommendation versus mandatory action distinction.

## Alternatives

- Treat all stress outputs as recommendations.
- Always require Founder review.
- Leave thresholds to implementation.

## Rationale

Capital governance requires clear escalation when runway, liquidity, concentration, or capital integrity risk is material.

## Risks

Thresholds may be set too conservatively or too loosely in later implementation.

## Consequences

Capital Stress Simulator, Treasury Risk Engine, and Portfolio Governance must preserve severity and mandatory review status.

## Enforcement

Critical stress can trigger emergency freeze according to policy; no stress output may move money autonomously.
