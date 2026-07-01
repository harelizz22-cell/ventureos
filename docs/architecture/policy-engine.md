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

Treasury Domain, Capital Lifecycle, Capital Allocation Governance, Milestone Funding, Portfolio Governance, Treasury Security, Treasury Risk Engine, Capital Stress Simulator, and Founder Financial Dashboard must route capital-sensitive actions through Policy Engine.

No money can move without Policy Engine evaluation.

## Consistency Requirements

Every governed request must record the policy version or policy snapshot evaluated.

If policy propagation is uncertain, required policy versions are missing, policy snapshots cannot be produced, or policy evaluators disagree, the affected request must fail closed.

Runtime components must not select the more permissive result when policy evaluators disagree.

Autonomy governance is enforced through Policy Engine evaluation. No autonomy escalation may occur without governance approval.

## Reliability Governance

Policy Engine evaluates reliability-sensitive actions including retry, compensation, rollback, forward recovery, Dead Letter escalation, circuit breaker override, incident response, and recovery replay where required.

Capital-sensitive, compliance-sensitive, customer-impacting, production-asset, or irreversible recovery must fail closed unless required approval and review are present.

## Enterprise Scale Enforcement

Policy Engine remains the enforcement point for tenant access, Organization boundaries, Portfolio boundaries, Venture boundaries, User access, Agent access, Capability access, Knowledge access, Global Search, Cross-Venture Intelligence, runtime access, memory access, Event subscription, analytics access, and AI context authorization.

No Organization may access another Organization's information unless explicitly governed.

Raw Venture data must not leak between Ventures unless Policy Engine explicitly allows it.

## Treasury Enforcement

Policy Engine evaluates capital-sensitive actions including reservation, commitment, approval, release, spend verification, recovery, cancellation, closure, emergency freeze, high-value approval, re-budgeting, holdback release, and freeze removal where required.

If policy, approval, lifecycle state, ledger state, treasury risk, or compliance status cannot be verified, the affected capital action must fail closed.
