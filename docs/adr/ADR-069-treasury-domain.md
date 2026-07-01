# ADR-069: Treasury Domain

Status: Accepted

Date: 2026-07-01

## Context

VentureOS requires institutional-grade capital protection before any implementation of allocation, funding, budgeting, or financial dashboard capabilities.

Recommendation systems already exist in architecture, but recommendation must remain separate from capital control.

## Decision

Adopt Treasury Domain as the only domain responsible for protecting, reserving, releasing, tracking, and reconciling capital.

Treasury never evaluates ideas, never creates strategy, never bypasses Policy Engine, and never autonomously moves money.

## Rationale

Capital discipline requires separation between business reasoning and financial control.

## Consequences

- Capital Allocation Engine and Investment Engine remain recommendation-only.
- Treasury owns financial lifecycle state and capital protection.
- Policy Engine governs Treasury actions.
- Founder retains final governance for capital-sensitive actions.

## Enforcement

No money can move without Policy Engine evaluation, applicable approval, audit record, and Treasury lifecycle state validation.
