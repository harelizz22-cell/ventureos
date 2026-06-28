# Audit Ledger Specification

Parent: `docs/contracts/agent-contracts.md`

Source Of Truth: This file is the source of truth for Audit Ledger contract requirements.

## Purpose

The Audit Ledger records meaningful system actions, state changes, approvals, denials, events, execution outcomes, and governance-relevant history.

## Scope

This specification defines the documentation contract for audit records. It does not define database schema, API endpoints, implementation code, or vendor-specific storage.

## Required Fields

- Audit ID
- Timestamp
- Actor
- Action
- Target
- Organization
- Portfolio
- Venture, if applicable
- Domain, if applicable
- Capability, if applicable
- Execution run, if applicable
- Event reference, if applicable
- Policy result, if applicable
- Evidence reference, if applicable
- Decision reference, if applicable
- Outcome

## Append-Only Rule

Audit is append-only. Audit entries cannot be edited.

Corrections must be recorded as new audit entries that reference the original entry.

## Relationship To Evidence And Decisions

Evidence, Decision, and Audit are separate architectural concerns.

Evidence must exist before Decision. Decision without Evidence is invalid. Audit records what happened and must not rewrite historical Evidence or Decision records.

## Future Database Mapping Note

Future database design must preserve append-only behavior, timestamp integrity, actor traceability, and relationship references.

## Future API Contract Note

Future API contracts must preserve append-only behavior and must not allow silent mutation of historical audit entries.

