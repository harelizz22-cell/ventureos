# ADR-060: Recovery Governance

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Recovery Governance decision.

## Status

Accepted

## Context

Recovery actions can touch assets, capital, customers, compliance-sensitive domains, audit history, and runtime state. Recovery must be governed rather than treated as a technical bypass.

## Decision

VentureOS adopts Recovery Governance as the source-of-truth architecture for recovery initiation, automatic recovery, governed recovery, Founder approval cases, compliance review cases, capital-sensitive recovery, recovery audit, recovery replay, and recovery safety.

## Alternatives considered

- Let Recovery Manager recover automatically whenever possible.
- Treat recovery as an implementation detail.
- Allow recovery to rewrite or hide failed execution history.

## Rationale

Governed recovery preserves safety, audit integrity, Founder authority, compliance boundaries, and capital discipline.

## Risks

- Recovery may be delayed by approval requirements.
- Recovery categories may need refinement during future implementation planning.
- Teams may confuse compensation with undoing history.

## Consequences

- Recovery is governed system behavior.
- Recovery may require Founder approval, compliance review, capital governance, and Evidence.
- Recovery replay must preserve historical Evidence, Decisions, Audit, and Event identity.

## Enforcement

Recovery must fail closed when policy, approval, Evidence, compliance review, capital sensitivity, idempotency, or recovery impact cannot be established.
