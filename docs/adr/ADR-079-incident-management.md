# ADR-079: Incident Management

Status: Accepted

Date: 2026-07-01

## Context

VentureOS must be able to detect, classify, own, escalate, recover, verify, audit, and learn from operational incidents.

## Decision

Adopt Incident Management architecture covering incident lifecycle, severity, priority, escalation, ownership, post-mortem, recovery verification, and audit linkage.

## Rationale

Operational incidents are governance events when they affect runtime, policy, capital, security, tenant isolation, evidence, decisions, audit, or Enterprise Value.

## Consequences

- Every incident has one accountable owner.
- Material incidents require post-mortem.
- Recovery must be verified before closure.
- Incident records are linked to Evidence, Decision, Audit, Event, Execution, and recovery records where applicable.

## Enforcement

Critical governance, capital, security, tenant isolation, audit integrity, or broad runtime incidents require Founder-visible escalation.
