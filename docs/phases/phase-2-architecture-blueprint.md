# Phase 2 Architecture Blueprint

Parent: `docs/phases/README.md`

Source Of Truth: This file is the source of truth for Phase 2 Architecture Blueprint scope.

## Purpose

Define the architecture work required before any implementation begins.

Phase 2 converts accepted findings from Claude Red Team Architecture Review into official VentureOS architecture workstreams. Claude review is not Source of Truth. Official Source of Truth remains `docs/architecture/`, accepted ADRs, and this phase blueprint.

## Objective

Close the critical architectural gaps identified by Red Team Review before system implementation.

## Status

Proposed. Documentation and architecture blueprint only.

No implementation is authorized by this document.

## Boundary

Phase 2 must not write production code, install dependencies, add integrations, add secrets, or authorize deployment.

Phase 2 defines architecture boundaries, ownership, failure modes, interactions, governance requirements, and acceptance criteria for later implementation phases.

Enterprise Value remains the primary objective. Founder governance remains non-negotiable.

## Workstream 1: Execution Orchestrator Decomposition

Status: Completed as Phase 2 Workstream 01 Runtime Kernel and Strategic Review Architecture.

Split the overloaded Execution Orchestrator into architectural sub-responsibilities:

- Execution Coordinator: Owns execution flow sequencing and implementation routing.
- Approval Coordinator: Owns approval waiting, approval state, timeout handling, and founder-visible pending decisions.
- Recovery Manager: Owns recovery trigger routing, compensation, rollback coordination, and recovery failure escalation.
- Event Coordinator: Owns event emission coordination, event ordering requirements, correlation, and replay coordination.
- Execution State Tracker: Owns execution state, state transitions, audit linkage, and runtime status visibility.
- Execution Scheduler: Owns governed scheduling, queue management, fairness, cost/resource/rate-limit awareness, and emergency pause support.
- Resource Coordinator: Owns pre-execution resource availability checks and coordination with Resource Domain, Cost Governance, Capital Allocation, Capital Reservation, Policy Engine, and Execution Scheduler.

Phase 2 must define boundaries, ownership, failure modes, and interactions for each responsibility.

No implementation is authorized.

Strategic Review Domain is documented as the recommendation layer for structured opportunity review. Runtime Kernel does not make business decisions.

## Workstream 1B: Enterprise Knowledge Graph, Organizational Memory, And Reasoning

Status: Completed as Phase 2 Workstream 01B Enterprise Knowledge Graph, Organizational Memory, and Reasoning Engine.

This workstream closes a Phase 2 architecture gap for long-term organizational intelligence before implementation begins.

- Enterprise Knowledge Graph defines the governed relationship layer across approved facts, Evidence, Decisions, Ventures, Markets, outcomes, risks, and architecture entities.
- Organizational Memory defines the durable historical memory layer for what happened and what VentureOS remembers.
- Reasoning Engine defines explainable reasoning and recommendation outputs from approved knowledge, memory, Evidence, and current context.
- Learning Engine remains separate and answers what VentureOS learned from outcomes.
- Knowledge Domain remains separate and owns knowledge assets and retrieval capabilities.

Reasoning outputs do not become Evidence automatically. They may become Candidate Evidence only through AI Output Classification and Evidence Promotion governance.

No new strategic concepts should be added until Phase 2 is completed and reviewed.

## Workstream 2: Policy Engine Consistency Model

Status: Completed as part of Phase 2 Workstream 02 Policy, Governance, Evidence, Autonomy, and Project Memory Sync.

Define the Policy Engine consistency model:

- Policy versioning.
- Policy snapshots.
- Policy propagation.
- Policy conflict handling.
- Policy evaluation consistency.
- Governance lag rules.
- Audit record for policy version used.
- Behavior when two policy evaluators disagree.

Every governed execution must record which policy version or policy snapshot was evaluated.

## Workstream 3: Evidence Freshness And Quality Model

Status: Completed as part of Phase 2 Workstream 02 Policy, Governance, Evidence, Autonomy, and Project Memory Sync.

Define the Evidence model for:

- Evidence freshness.
- Evidence expiration.
- Evidence quality tiers.
- Source quality.
- Confidence.
- Corroboration requirements.
- Stale evidence handling.
- Evidence suitability by decision category.

Evidence used for Decisions must identify freshness and quality status where meaningful.

## Workstream 4: Autonomy Governance Model

Status: Completed as part of Phase 2 Workstream 02 Policy, Governance, Evidence, Autonomy, and Project Memory Sync.

Define runtime autonomy governance:

- Autonomy levels.
- Allowed actions per level.
- Blocked actions per level.
- Promotion rules.
- Demotion rules.
- Safe mode.
- Emergency mode.
- Partial autonomy per Domain, Capability, Venture, and Organization.
- Runtime enforcement through Policy Engine.

Autonomy never overrides governance, Evidence, approval, audit, recovery, or Founder authority.

## Workstream 5: AI Output Classification

Status: Completed as part of Phase 2 Workstream 02 Policy, Governance, Evidence, Autonomy, and Project Memory Sync.

Define the AI output lifecycle:

Draft -> Recommendation -> Candidate Evidence -> Verified Evidence

AI output must never enter Evidence Ledger directly without promotion governance.

Promotion must require source review, confidence assessment, evidence quality evaluation, and auditability.

## Workstream 6: Event Ordering And Replay Model

Status: Completed as part of Phase 2 Workstream 02 Policy, Governance, Evidence, Autonomy, and Project Memory Sync.

Define event ordering and replay architecture:

- Event envelope.
- Per-entity ordering.
- Deduplication.
- Replay.
- Schema versioning.
- Audit behavior on duplicate events.
- Audit behavior on out-of-order events.
- Recovery usage.

Replay must preserve audit integrity and must not rewrite historical Decisions.

## Workstream 7: Cross-Venture Query Governance

Status: Completed as part of Phase 2 Workstream 04 Enterprise Scale Architecture.

Define governed portfolio-wide intelligence for:

- Business Intelligence.
- Learning Engine.
- Capital Allocation Engine.
- Portfolio Diversification.
- Opportunity Score.
- Enterprise Value Engine.

The model must preserve venture isolation while allowing governed aggregate intelligence.

Cross-venture queries must be scoped, policy-evaluated, auditable, and restricted by Organization, Portfolio, Venture, Domain, Capability, and role where required.

## Workstream 8: Founder Unavailability And Governance Escalation

Define Founder unavailability behavior without creating a Deputy Founder model:

- Founder timeout.
- Emergency governance mode.
- Fail-closed behavior.
- Escalation rules.
- Pending decision handling.
- Recovery after Founder returns.

Founder unavailability must not become a backdoor for system self-approval.

## Workstream 9: Learning Quarantine Model

Define learning state controls:

- Disputed learning record.
- Quarantined learning record.
- Withdrawn learning record.
- Impact on future recommendations.
- Audit preservation.
- Rollback of learning influence.

Learning quarantine must preserve historical audit while preventing disputed learning from silently influencing future recommendations.

## Workstream 10: Compliance Gate Runtime Mechanism

Define Compliance Gate as enforceable runtime architecture:

- Compliance Gate Registry.
- Policy Engine evaluation.
- Restricted capability categories.
- Legal approval records.
- Investment marketplace gating.
- Regulated domain gating.

Compliance Gate must apply to regulated domains, investor marketplace capabilities, securities-related activity, medical, financial, biotech, and other enhanced-review areas.

No regulated financial activity is approved by Phase 2.

## Workstream 11: Multi-Tenancy Isolation Model

Status: Completed as part of Phase 2 Workstream 04 Enterprise Scale Architecture.

Define isolation architecture:

- Organization isolation.
- Portfolio isolation.
- Venture isolation.
- Data access boundaries.
- Cross-organization access rules.
- Breach response model.

Multi-tenancy must preserve explicit `organization_id`, `portfolio_id`, and `venture_id` scope.

## Workstream 12: Capital Reservation And Conflict Model

Define capital reservation architecture:

- Capital reservations.
- Competing allocations.
- Reservation expiry.
- Approval race conditions.
- Overcommit prevention.
- Allocation audit.

Capital reservations are governance records. They do not move money and do not execute investments.

## Workstream 13: Exit Management Capability

Define Exit Management as a governed cross-domain Capability group. Do not create an Exit Domain yet.

Exit Management must cover:

- Sale.
- Acquisition.
- Shutdown.
- Archive.
- IP transfer.
- Asset transfer.
- Final audit.
- Irreversibility declaration.

Exit Management must preserve Evidence, Decision, Audit, Founder approval, legal/compliance review, recovery constraints, and asset ownership requirements.

## Workstream 14: Legal And Compliance Runtime Domain Planning

Define future Legal and Compliance runtime concerns:

- Policies.
- Events.
- Review triggers.
- Approval requirements.
- Enhanced review for medical, financial, securities, biotech, and regulated domains.

This is planning only. No legal advice, licensing, regulated workflow, or implementation is approved.

## Workstream 15: Opportunity Score Audit And Bias Detection

Define Opportunity Score audit requirements:

- Score explainability.
- Evidence used.
- Weightings.
- Model version.
- Bias review.
- Score audit trail.

Opportunity Score must remain governed comparison and must not override Founder approval, Investment Readiness, Thesis alignment, Evidence, or compliance gates.

## Workstream 16: Audit Ledger Query Model

Define Audit Ledger query architecture:

- Query requirements.
- Access control.
- Export model.
- Retention.
- Legal chain of custody.
- Investor/regulator review support.

Audit query capability must preserve append-only integrity and access governance.

## Workstream 17: Recovery Governance Model

Status: Completed as part of Phase 2 Workstream 03 Execution Reliability.

Define Recovery as governed architecture:

- Recovery actions pass through Policy Engine where required.
- Compensation versus rollback.
- Recovery audit records.
- Recovery failure handling.
- Recovery escalation.

Recovery must not bypass governance, Evidence, approval, audit, cost, compliance, or Founder authority.

## Workstream 18: Agent Evolution Governance

Define agent evolution governance:

- Agent promotion.
- Agent rollback.
- Capability expansion.
- Evidence requirements.
- Approval requirements.
- Audit requirements.
- Autonomy constraints.

Agents cannot approve their own evolution, expand their own permissions, or raise their own autonomy level.

## Acceptance Criteria

- Each workstream has source-of-truth architecture documentation or approved ADR coverage before implementation.
- Execution Orchestrator sub-responsibility boundaries are defined.
- Policy Engine consistency and policy snapshot rules are defined.
- Evidence freshness and quality requirements are defined.
- Autonomy governance is enforceable through Policy Engine.
- AI output promotion governance is defined.
- Event ordering, deduplication, replay, and schema versioning rules are defined.
- Cross-venture queries preserve venture isolation.
- Founder unavailability behavior fails closed unless explicitly governed.
- Learning quarantine prevents disputed learning from silently influencing recommendations.
- Compliance Gate runtime mechanism is defined.
- Multi-tenancy isolation and breach response model are defined.
- Capital reservation conflict rules are defined.
- Exit Management is defined as a governed cross-domain Capability group.
- Legal and Compliance runtime planning is documented.
- Opportunity Score audit and bias detection are defined.
- Audit Ledger query model is defined.
- Recovery governance is defined.
- Agent evolution governance is defined.

## Non-Goals

- No production code.
- No dependency installation.
- No external integrations.
- No deployment.
- No secrets.
- No regulated financial workflows.
- No autonomous money movement.
- No Deputy Founder model.
- No Exit Domain.

## Open Questions

- Which workstreams must be completed before Phase 1 implementation approval?
- Which workstreams belong in Phase 2 versus Phase -1 architecture foundation?
- What minimum policy snapshot model is required for first implementation?
- What evidence freshness tiers are required for MVP governance?
- What safe mode behavior should be Founder-visible first?
- What audit export requirements are needed for legal, investor, and regulator review?
