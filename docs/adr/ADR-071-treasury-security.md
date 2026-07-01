# ADR-071: Treasury Security

Status: Accepted

Date: 2026-07-01

## Context

Capital workflows require stronger security than ordinary recommendation or analysis workflows because they create financial, governance, fraud, and audit risk.

## Decision

Adopt Treasury Security requirements for multi-step approvals, segregation of duties, cryptographic audit trail, immutable financial ledger, tamper detection, fraud detection, anomaly detection, high-value approval workflow, and emergency lock.

## Rationale

Financial architecture must assume unauthorized access, tampering, duplicate allocation, and unsafe automation are core risks.

## Consequences

- Recommendation systems cannot release capital.
- AI outputs cannot approve financial action.
- Emergency lock fails closed and must be Founder-visible.
- Historical financial records must be immutable.

## Enforcement

High-value, anomalous, tamper-suspected, fraud-suspected, or policy-uncertain financial actions require lock, denial, or governed escalation.
