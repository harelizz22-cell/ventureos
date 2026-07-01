# ADR-074: Treasury Risk Engine

Status: Accepted

Date: 2026-07-01

## Context

Capital allocation and funding decisions require financial risk evaluation before capital is reserved, committed, approved, or released.

## Decision

Adopt Treasury Risk Engine to evaluate cash runway, concentration risk, capital depletion, funding dependency, market downturn simulation, unexpected cost growth, and budget overruns.

## Rationale

Governed capital decisions require risk visibility before financial action, not after losses occur.

## Consequences

- High-risk capital actions require governed review.
- Risk output is a signal or recommendation, not a final Decision.
- Risk assumptions and data freshness must be recorded.

## Enforcement

Capital-sensitive execution must fail closed when required Treasury Risk Engine inputs cannot be evaluated.
