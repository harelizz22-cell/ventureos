# Architecture Principles

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for non-negotiable VentureOS architecture principles.

## Purpose

Define the non-negotiable architecture principles of VentureOS.

These principles guide architecture review, phase planning, implementation approval, runtime governance, and future system evolution.

## 1. Enterprise Value Above All

Definition: VentureOS optimizes for long-term Enterprise Value across Organizations, Portfolios, and Ventures.

Why it matters: Revenue, activity, output volume, and agent productivity are useful only when they contribute to durable Enterprise Value.

Enforcement rule: Architecture and implementation decisions must explain their expected Enterprise Value contribution or explicitly justify why the work is foundational.

## 2. Evidence Before Decision

Definition: Meaningful Decisions must be based on recorded Evidence.

Why it matters: Evidence protects Founder judgment, improves auditability, reduces unsupported action, and makes later review possible.

Enforcement rule: Decisions without required Evidence are invalid and must not authorize governed execution.

## 3. Capabilities Before Agents

Definition: VentureOS is capability-first. Agents are implementation options, not the architecture model.

Why it matters: Capabilities preserve durable system design while allowing humans, agents, APIs, internal services, and future engines to remain interchangeable.

Enforcement rule: Every Agent must execute approved Capabilities and must not define, own, or bypass Capability architecture.

## 4. Policy Before Execution

Definition: Governed execution must pass Policy Engine evaluation before action.

Why it matters: Policy prevents unauthorized action, uncontrolled spending, self-approval, and governance drift.

Enforcement rule: No Capability, Agent, Workflow, Tool, Service, or External Provider may self-approve execution.

## 5. Governance Before Autonomy

Definition: Autonomy expands only after governance, evidence, approval, audit, monitoring, and recovery requirements are satisfied.

Why it matters: Autonomy without governance creates unmanaged operational, financial, legal, and founder-control risk.

Enforcement rule: Autonomy promotion requires approved evidence and must be enforceable through Policy Engine rules.

## 6. Founder Control Is Preserved

Definition: Founder authority remains the highest authority in VentureOS.

Why it matters: VentureOS exists to increase founder leverage without surrendering ownership, control, assets, or final authority.

Enforcement rule: Architecture must not create hidden ownership, uncontrolled approvals, irreversible action without governance, or system self-approval.

## 7. Capital Is A Limited Resource

Definition: Capital, budgets, tokens, infrastructure, time, and attention are governed Resources.

Why it matters: Resource discipline preserves survival, prevents waste, and keeps execution tied to expected business value.

Enforcement rule: Capital allocation and resource-consuming execution must include Evidence, expected ROI where meaningful, risk, approval requirements, and auditability.

## 8. Every Action Is Auditable

Definition: Meaningful actions, decisions, state changes, approvals, denials, executions, events, policy outcomes, and recovery actions must be auditable.

Why it matters: Auditability makes trust, recovery, review, governance, investor explanation, and regulatory readiness possible.

Enforcement rule: Meaningful runtime behavior must produce append-only Audit records or documented audit-equivalent records.

## 9. Learn From Every Outcome

Definition: VentureOS converts outcomes into evidence-backed, auditable learning.

Why it matters: Successful ventures, failed ventures, killed opportunities, founder overrides, budget decisions, and recovery events should improve future recommendations.

Enforcement rule: Learning updates must be evidence-backed, auditable, and subject to quarantine or withdrawal when disputed.

## 10. Long-Term Enterprise Value Beats Short-Term Profit

Definition: Short-term profit is important, but it must not override long-term Enterprise Value.

Why it matters: Durable value may require defensibility, learning, brand, assets, customer base, operational maturity, and risk reduction.

Enforcement rule: Scoring, capital allocation, investment, and strategic recommendations must distinguish short-term profit from long-term Enterprise Value.

## 11. No Execution Without Scope

Definition: Every governed action must carry explicit Organization, Portfolio, and Venture scope where applicable.

Why it matters: Explicit scope preserves multi-tenancy, venture isolation, auditability, and cross-venture governance.

Enforcement rule: No global default Venture scope is allowed for Capability invocation, Execution, Evidence, Decision, Audit, Event, Tool call, AI call, Asset, Cost record, or Investment recommendation.

## 12. No Autonomous Money Movement Without Governance

Definition: VentureOS must not autonomously transfer money, execute investments, or perform regulated financial activity without approved governance and legal/compliance structure.

Why it matters: Money movement creates financial, legal, operational, and Founder-control risk.

Enforcement rule: Capital Allocation, Investment, Funding, Marketplace, and Milestone Capital Release components may recommend but must not move money or execute investments without explicit approved governance.

## 13. Compliance Gates Are Runtime Controls

Definition: Compliance gates must be enforceable runtime architecture, not advisory text only.

Why it matters: Regulated domains, securities, medical, biotech, financial, investor marketplace, and enhanced-review activities require enforceable restrictions.

Enforcement rule: Restricted Capability categories must pass Compliance Gate and Policy Engine evaluation before execution.

## 14. AI Outputs Are Not Evidence Until Promoted

Definition: AI output starts as Draft, Recommendation, or Candidate Evidence and becomes Verified Evidence only through promotion governance.

Why it matters: AI output can be useful but must not weaken Evidence Ledger integrity or decision quality.

Enforcement rule: AI output must never enter Evidence Ledger directly without source review, confidence assessment, evidence quality evaluation, and required approval.

## 15. Recovery Is Governed

Definition: Recovery actions are governed system behavior and must not bypass Policy, Evidence, approval, audit, cost, compliance, or Founder authority.

Why it matters: Recovery often touches assets, state, data, costs, and irreversible operational choices.

Enforcement rule: Recovery actions must pass Policy Engine evaluation where required and must produce recovery audit records.

## Phase 2 Status

Phase 2 starts with these Architecture Principles as the governing baseline.

The next Phase 2 workstream is Founder Unavailability and Governance Escalation.
