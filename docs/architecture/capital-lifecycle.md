# Capital Lifecycle

Parent: `docs/architecture/treasury-domain.md`

Source Of Truth: This file is the source of truth for Capital Lifecycle architecture.

## Purpose

Capital Lifecycle defines the required states every dollar must pass through so VentureOS can prevent double allocation, preserve auditability, and maintain capital discipline.

Every dollar has a lifecycle. Every capital movement must be auditable.

## Lifecycle States

### Available

Capital that is not reserved, committed, approved, released, or spent.

Required controls:

- Must be reconciled.
- Must be visible to Treasury and Founder Financial Dashboard.
- Must not include capital already reserved elsewhere.

### Reserved

Capital temporarily held for a proposed allocation without moving money.

Required controls:

- Must reference an approved or pending capital request.
- Must have reservation amount, expiry, scope, and owner.
- Must prevent the same capital from being reserved twice.

### Committed

Capital assigned to a governed plan after approval path is identified.

Required controls:

- Must reference Decision, Evidence, Policy Engine result, and approval requirements.
- Must not be released until release criteria are satisfied.

### Approved

Capital approved for release subject to lifecycle, milestone, compliance, and Treasury checks.

Required controls:

- Must include approving authority.
- Must include policy version or snapshot.
- Must include amount, scope, and constraints.

### Released

Capital made available for authorized spend or execution under the approved scope.

Required controls:

- Must pass Policy Engine.
- Must reference approved reservation or commitment.
- Must record release amount, timing, recipient scope, and release authority.

### Spent

Capital recorded as consumed.

Required controls:

- Must include spend evidence, categorization, and budget association.
- Must be reconciled against release and approval.

### Verified

Spent capital confirmed against evidence, receipt, ledger record, or approved verification process.

Required controls:

- Must preserve verification evidence.
- Must identify variance, exception, or mismatch.

### Recovered

Capital returned, clawed back, refunded, or otherwise recovered.

Required controls:

- Must reference original release or spend.
- Must identify reason, recovery method, and resulting available or closed state.

### Cancelled

Capital request, reservation, commitment, or release path terminated before completion.

Required controls:

- Must release unused reserved capital back to Available or other governed state.
- Must record cancellation reason and authority.

### Closed

Capital lifecycle record completed and no longer active.

Required controls:

- Must preserve final state, audit trail, evidence, decisions, and reconciliation status.

## Transition Rules

- No money can move without Policy Engine evaluation.
- No capital can be allocated twice.
- State transitions must preserve previous state and append a new record.
- Founder approval is required for high-value, exceptional, irreversible, or policy-defined capital actions.
- Treasury must fail closed when lifecycle state, approval state, policy state, or ledger state is inconsistent.

## Audit Requirements

Each transition must record:

- Prior state.
- New state.
- Amount.
- Organization, Portfolio, Venture, and budget scope.
- Actor.
- Policy version or snapshot.
- Approval record.
- Evidence and Decision links.
- Timestamp.
- Correlation ID.
- Exception or override reason where applicable.

## Placeholder Status

This is architecture documentation only. It does not define schemas, ledger implementation, financial integrations, payment execution, custodial services, or securities workflows.
