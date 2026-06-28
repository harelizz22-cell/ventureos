# ADR-008: Domain-First Capability Model

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Domain-first capability model decision.

## Status

Accepted

## Context

Capability-first architecture needs a business structure so capabilities do not become an unbounded list.

## Decision

VentureOS adopts Business Domains.

Initial Domains are Research, Validation, Build, Marketing, Sales, Finance, Operations, Legal, Governance, Knowledge, Identity, Resources, and Analytics.

Every Domain owns Capabilities, Policies, Events, Workflows, Data, Interfaces, and Future implementations.

## Consequences

- Capabilities must belong to Domains.
- Knowledge, Identity, and Resources receive architecture placeholders.
- Domain ownership becomes part of future phase and capability specification.

## Enforcement

Capability definitions must identify their owning Domain before implementation.

