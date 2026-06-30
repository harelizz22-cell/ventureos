# Policy Engine

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Policy Engine architecture.

## Purpose

The Policy Engine evaluates proposed actions against governance rules.

Policy consistency requirements are defined in `docs/architecture/policy-engine-consistency-model.md`.

## Outcomes

- Allow.
- Deny.
- Require evidence.
- Require founder approval.
- Require risk review.
- Require auditor review.
- Require rollback plan.
- Require recovery plan.
- Require compensation review.
- Require incident creation.

## Decision Outcomes

The Policy Engine must express governed responses using these decision outcomes:

- Approved.
- Denied.
- Pending Founder Approval.
- Pending Delegated Approval.
- Blocked By Governance.
- Fail Closed.

The Execution Orchestrator owns waiting and continuation behavior after Policy Engine response.

## Rule

Policies must be explicit, versioned, testable, and auditable.

Execution API must request Policy Engine evaluation before accepted requests enter Runtime Kernel.

All execution paths must pass through the Policy Engine.

No Capability, Agent, Workflow, Tool, Service, or External Provider may self-approve execution.

If the Policy Engine is unavailable, VentureOS must fail closed. No execution is permitted while governance is unavailable.

At startup, the Execution Orchestrator must not accept execution requests until Policy Engine health is confirmed.

If the Policy Engine becomes unavailable, new execution must stop fail-closed.

Cost Governance may be used as an approval input.

## Consistency Requirements

Every governed request must record the policy version or policy snapshot evaluated.

If policy propagation is uncertain, required policy versions are missing, policy snapshots cannot be produced, or policy evaluators disagree, the affected request must fail closed.

Runtime components must not select the more permissive result when policy evaluators disagree.

Autonomy governance is enforced through Policy Engine evaluation. No autonomy escalation may occur without governance approval.

## Reliability Governance

Policy Engine evaluates reliability-sensitive actions including retry, compensation, rollback, forward recovery, Dead Letter escalation, circuit breaker override, incident response, and recovery replay where required.

Capital-sensitive, compliance-sensitive, customer-impacting, production-asset, or irreversible recovery must fail closed unless required approval and review are present.
