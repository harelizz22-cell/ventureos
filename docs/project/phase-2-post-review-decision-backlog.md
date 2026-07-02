# Phase 2 Post-Review Decision Backlog

Parent: `docs/project/project-dashboard.md`

Source Of Truth: This file is the source of truth for implementation-gated decisions identified after Phase 2 Claude Red Team Review.

## Purpose

Record architecture decisions that do not block Phase 2 closure but must be resolved before affected implementation work begins.

Claude review is not Source of Truth. These backlog items become governing only when accepted through future ADRs, phase documents, or implementation planning decisions.

## Current Status

Status: Not blocking Phase 2 closure; blocking affected implementation.

Phase 3 has not started.

## Backlog Items

### Policy Engine Warm-Up And Cold-Start Behavior

Why it matters: Policy Engine must not accept execution before policy availability, snapshot readiness, evaluator readiness, and fail-closed behavior are verified.

Affected components: Policy Engine, Runtime Kernel, Execution API, Execution Scheduler, Observability, Incident Management.

Required before which implementation: Policy Engine runtime implementation, Runtime Kernel startup implementation, Execution API request acceptance.

Current status: Not blocking Phase 2 closure; blocking affected implementation.

### Cross-Organization Audit Access For Regulatory Review

Why it matters: Regulatory or compliance review may require governed access across Organizations without weakening tenant isolation or data ownership.

Affected components: Audit Ledger, Enterprise Isolation, Data Ownership Model, Enterprise Identity Model, Policy Engine, Compliance Gate.

Required before which implementation: Cross-Organization audit review tooling, regulatory export, compliance reviewer access.

Current status: Not blocking Phase 2 closure; blocking affected implementation.

### Dead Letter Ownership And Resolution Authority

Why it matters: Failed executions must have a clear owner, escalation path, and resolution authority so Dead Letter queues do not become unmanaged operational debt.

Affected components: Execution Reliability, Runtime Kernel, Recovery Governance, Incident Management, Policy Engine, Operations Dashboard.

Required before which implementation: Dead Letter queue runtime, incident workflow, recovery operations.

Current status: Not blocking Phase 2 closure; blocking affected implementation.

### Evidence Ledger Write Authority Model

Why it matters: Evidence integrity depends on explicit authority for who or what may write, promote, reject, defer, or amend Evidence records.

Affected components: Evidence Ledger, AI Output Classification, Evidence Freshness and Quality Model, Policy Engine, Audit Ledger, Reasoning Engine.

Required before which implementation: Evidence Ledger write API, Evidence Promotion Queue, AI evidence promotion workflow.

Current status: Not blocking Phase 2 closure; blocking affected implementation.

### Minimum Viable Evidence Threshold By Decision Category

Why it matters: Different Decisions require different evidence strength, freshness, corroboration, and review levels; weak evidence must not support high-risk Decisions.

Affected components: Evidence Freshness and Quality Model, Evidence Ledger, Policy Engine, Strategic Review Domain, Capital Allocation Governance.

Required before which implementation: Decision workflows, Strategic Review execution, capital-sensitive approvals, autonomy promotion.

Current status: Not blocking Phase 2 closure; blocking affected implementation.

### Audit Record Ownership During Venture Transfer

Why it matters: When a Venture transfers between Portfolios or Organizations, audit ownership, visibility, retention, and access must remain governed and traceable.

Affected components: Audit Ledger, Data Ownership Model, Enterprise Isolation, Portfolio Governance, Venture Timeline, Enterprise Knowledge Graph.

Required before which implementation: Venture transfer workflows, Portfolio restructuring, Organization migration, cross-Organization transfer.

Current status: Not blocking Phase 2 closure; blocking affected implementation.
