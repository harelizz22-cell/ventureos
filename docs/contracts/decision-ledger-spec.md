# Decision Ledger Specification

Parent: `docs/contracts/agent-contracts.md`

Source Of Truth: This file is the source of truth for Decision Ledger contract requirements.

## Purpose

The Decision Ledger records meaningful VentureOS decisions in a durable, auditable format.

## Scope

This specification defines the documentation contract for decision records. It does not define database schema, API endpoints, implementation code, or vendor-specific storage.

## Required Fields

- Decision ID
- Date
- Title
- Decision owner
- Status
- Context
- Options considered
- Evidence references
- Decision
- Approval record
- Expected outcome
- Revisit trigger
- Rollback criteria
- Related ADR, if applicable
- Related runtime decision, if applicable

## Immutability Rule

Decision records must not be silently overwritten. Corrections, superseding decisions, reversals, and follow-up decisions must preserve the original record and create an auditable change trail.

## Audit Requirements

Every decision record must identify who made the decision, what evidence was used, what approval was required, when the decision occurred, and when the decision should be revisited.

## Relationship To ADRs

ADRs record architecture decisions. The Decision Ledger may reference ADRs, but it does not replace them. Architecture-changing decisions still require ADR workflow compliance.

## Relationship To Runtime Decisions

Runtime decisions are operational decisions made while VentureOS is operating. Runtime decision records must link back to this Decision Ledger contract when they are meaningful, governed, or auditable.

## Future Database Mapping Note

Future database design must map these required fields without weakening immutability, auditability, or relationship requirements.

## Future API Contract Note

Future API contracts must preserve the same required fields, audit requirements, and immutability behavior defined here.

