# ADR-036: Policy Engine Consistency Required

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Policy Engine consistency decision.

## Status

Accepted

## Context

Governed execution must be auditable and repeatable enough to explain why a policy decision happened. Without policy versioning and snapshots, decisions may become ambiguous when policies change.

## Decision

VentureOS requires Policy Engine consistency architecture before implementation.

Policy decisions must account for policy versioning, policy snapshots, propagation, conflict handling, evaluation consistency, governance lag, and audit record for policy version used.

## Consequences

- Every governed execution must record the policy version or snapshot evaluated.
- Policy conflicts and propagation lag become architecture concerns.
- Audit records must preserve policy evaluation context.

## Enforcement

No governed runtime implementation may proceed without policy consistency rules sufficient for audit, recovery, and Founder review.
