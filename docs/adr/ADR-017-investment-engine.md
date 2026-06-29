# ADR-017: Investment Engine

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Investment Engine decision.

## Status

Accepted

## Context

VentureOS must eventually evaluate internal venture opportunities and external investment opportunities without executing financial actions autonomously.

## Decision

VentureOS adopts an Investment Engine for evaluating internal and external investment opportunities.

## Consequences

- External startup investment evaluation is a future architecture requirement.
- The system may discover, analyze, score, compare, recommend, track, and recommend exits.
- Financial execution always requires Founder-defined governance.

## Enforcement

The Investment Engine never executes investments. It generates governed recommendations only.

