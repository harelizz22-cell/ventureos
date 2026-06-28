# ADR-006: Organization Layer

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Organization layer decision.

## Status

Accepted

## Context

VentureOS requires a durable ownership and operating boundary above Portfolios and Ventures.

## Decision

Organization is adopted as a first-class architectural entity.

The hierarchy is:

Founder -> Organization -> Portfolio -> Venture -> Domain -> Capability -> Workflow -> Execution -> Evidence -> Decision -> Audit

## Consequences

- Organization becomes the parent context for Portfolios, Ventures, assets, identities, resources, policies, evidence, decisions, and audit.
- Future architecture must identify Organization scope where relevant.
- Founder ownership remains above Organization.

## Enforcement

New architecture work must not bypass Organization when defining ownership, resource, identity, or audit boundaries.

