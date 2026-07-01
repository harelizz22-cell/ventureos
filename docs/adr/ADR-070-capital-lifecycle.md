# ADR-070: Capital Lifecycle

Status: Accepted

Date: 2026-07-01

## Context

VentureOS must prevent double allocation and must make every dollar traceable across reservation, approval, release, spend, verification, recovery, cancellation, and closure.

## Decision

Adopt Capital Lifecycle states: Available, Reserved, Committed, Approved, Released, Spent, Verified, Recovered, Cancelled, and Closed.

Every dollar has a lifecycle. Every capital movement must be auditable.

## Rationale

Capital movement without lifecycle state creates overcommit, reconciliation, audit, and governance risk.

## Consequences

- Capital cannot be counted as available once reserved, committed, approved, released, or spent.
- Corrections must create new auditable records instead of editing history.
- Financial state must be visible to Treasury and Founder Financial Dashboard.

## Enforcement

Treasury must fail closed when lifecycle state, approval state, policy state, or ledger state is inconsistent.
