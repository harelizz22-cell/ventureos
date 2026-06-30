# ADR-064: Data Ownership Model

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Data Ownership Model decision.

## Status

Accepted

## Context

Enterprise-scale VentureOS needs clear ownership for Organizations, Portfolios, Ventures, Evidence, Decisions, Knowledge, Memory, graph records, Assets, AI Outputs, Events, and Audit records.

## Decision

VentureOS adopts a Data Ownership Model requiring every object to have one clear owner while preserving policy, authorization, audit, Evidence, and Decision boundaries.

## Alternatives

- Let ownership be inferred from storage location.
- Allow shared ownership for business objects.
- Treat ownership as equivalent to unrestricted access.

## Rationale

Clear ownership prevents ambiguity, supports recovery, strengthens governance, and reduces cross-tenant data risk.

## Risks

- Ownership rules may need refinement for future legal entities or customer accounts.
- Asset ownership may require stricter legal/compliance review.
- Teams may confuse ownership with access permission.

## Consequences

- Every object must identify one owner.
- Access remains governed by Policy Engine and authorization.
- Owners cannot rewrite historical Evidence, Decisions, or Audit records.

## Enforcement

Future implementation must not create ownerless or ambiguously owned governed objects.
