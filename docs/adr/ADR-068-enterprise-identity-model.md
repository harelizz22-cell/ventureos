# ADR-068: Enterprise Identity Model

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Enterprise Identity Model decision.

## Status

Accepted

## Context

Enterprise-scale VentureOS requires explicit identities for Founder, Organization, Portfolio, Venture, Human Users, AI Agents, Runtime Services, External Systems, future Investors, and future Partners.

## Decision

VentureOS adopts Enterprise Identity Model and separates authentication from authorization.

## Alternatives

- Treat identity as only human user accounts.
- Let implementation define service, agent, and external identities later.
- Treat authentication as sufficient for access.

## Rationale

Explicit identity supports auditability, isolation, policy evaluation, access control, and future enterprise/customer operation.

## Risks

- Identity scope may become complex across Organizations, Portfolios, and Ventures.
- Future Investor and Partner identities may be mistaken for active capability.
- Runtime Service identity may be confused with actor authority.

## Consequences

- All identities must be explicit, scoped, auditable, and authorization-bound.
- Authentication verifies identity.
- Authorization determines allowed access and action.
- Policy Engine remains the runtime enforcement point for governed authorization.

## Enforcement

Authentication alone never grants access or execution authority.
