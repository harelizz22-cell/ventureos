# Policy Engine

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Policy Engine architecture.

## Purpose

The Policy Engine evaluates proposed actions against governance rules.

## Outcomes

- Allow.
- Deny.
- Require evidence.
- Require founder approval.
- Require risk review.
- Require auditor review.
- Require rollback plan.

## Rule

Policies must be explicit, versioned, testable, and auditable.

All execution paths must pass through the Policy Engine.

No Capability, Agent, Workflow, Tool, Service, or External Provider may self-approve execution.

If the Policy Engine is unavailable, VentureOS must fail closed. No execution is permitted while governance is unavailable.

Cost Governance may be used as an approval input.
