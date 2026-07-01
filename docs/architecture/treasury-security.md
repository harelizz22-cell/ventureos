# Treasury Security

Parent: `docs/architecture/treasury-domain.md`

Source Of Truth: This file is the source of truth for Treasury Security architecture.

## Purpose

Treasury Security protects financial actions, lifecycle records, approvals, and audit trails from unauthorized access, fraud, tampering, and unsafe automation.

## Multi-Step Approvals

Capital-sensitive actions require multiple checks before execution or state transition:

- Actor identity and role validation.
- Policy Engine evaluation.
- Evidence and Decision linkage.
- Budget and lifecycle verification.
- Founder or delegated approval where policy requires it.

## Segregation Of Duties

No single actor or component should control recommendation, approval, release, verification, and audit for the same capital action.

Rules:

- Recommendation systems do not release capital.
- Treasury does not evaluate ideas or create strategy.
- Auditors do not approve their own findings.
- AI outputs do not approve financial action.

## Cryptographic Audit Trail

Treasury records must be tamper-evident.

Required properties:

- Append-only financial action history.
- Integrity checks for state transitions.
- Linkage between Evidence, Decision, Policy, Audit, and lifecycle state.
- Tamper alerts for missing, modified, or inconsistent records.

## Immutable Financial Ledger

Financial lifecycle records must be immutable after creation.

Corrections must be new entries that reference the prior record and explain the correction.

## Tamper Detection

Tamper detection must monitor:

- Missing approvals.
- Ledger gaps.
- Changed historical records.
- Mismatched state transitions.
- Unauthorized actor access.
- Duplicate or conflicting allocation records.

## Fraud Detection

Fraud detection must monitor:

- Unusual release timing.
- Unusual release size.
- Repeated failed approval attempts.
- Actor behavior anomalies.
- Vendor, recipient, or destination irregularities where future implementation supports them.

## Anomaly Detection

Anomaly detection must surface unusual patterns across budgets, releases, spend, recovery, reserves, runway, and portfolio concentration.

Anomaly findings are signals. They do not become Evidence automatically unless promoted through governed Evidence processes.

## High-Value Approval Workflow

High-value actions require:

- Strong actor authentication.
- Policy Engine approval or founder-visible pending approval.
- Additional reviewer or Founder approval where policy requires it.
- Treasury lifecycle verification.
- Audit record before and after action.

## Emergency Lock

Emergency lock stops affected capital actions when fraud, tampering, identity compromise, Policy Engine failure, compliance uncertainty, or ledger inconsistency is detected.

Rules:

- Emergency lock fails closed.
- Emergency lock must be Founder-visible.
- Unlock requires governed review and audit.

## Placeholder Status

This is architecture documentation only. It does not define cryptographic implementation, key management, payment rails, account systems, secrets, integrations, or production code.
