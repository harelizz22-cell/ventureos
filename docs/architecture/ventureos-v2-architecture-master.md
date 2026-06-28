# VentureOS v2 Architecture Master

## 1. Mission

VentureOS exists to help a founder discover, validate, launch, operate, optimize, and scale profitable digital businesses while preserving founder ownership, auditability, and control.

## 2. Vision

The long-term system is a founder-governed autonomous venture operating system. It can coordinate agents, workflows, tools, evidence, decisions, assets, recovery plans, and financial constraints across a portfolio of ventures.

## 3. Current Stage

The current stage is architecture foundation. The operating mode is Autonomy Level 1: Assisted Mode. No production application code is approved at this stage.

## 4. Core Architecture Position

The architecture must be 100% autonomy-ready while initial configuration remains conservative. Autonomy capabilities are designed into the system, but activation is gated by governance, policy, evidence, approvals, and audit trails.

## 5. Autonomy Model

- Level 0: Manual. Humans perform and approve all actions.
- Level 1: Assisted. Agents draft, analyze, recommend, and prepare actions. Humans approve meaningful execution.
- Level 2: Semi-Autonomous. Agents may execute bounded actions under explicit policies and thresholds.
- Level 3: Autonomous. Agents may execute approved workflows with monitoring, rollback, and exception handling.
- Level 4: Portfolio Mode. The system coordinates multiple ventures with portfolio-level capital, risk, and resource policies.

The initial system configuration is Level 1.

## 6. Design Principles

- Evidence before action.
- No build before validation.
- Profit before activity.
- Survival before growth.
- Founder owns all assets.
- No agent self-approval.
- No agent self-modification.
- No direct external tool access by agents.
- Tool access only through Tool Gateway.
- AI model access only through AI Gateway.
- Spending above configured thresholds requires approval.
- No secrets in prompts, logs, commits, or documentation.
- Every meaningful decision must be auditable.
- Every production asset must have owner, backup, rollback, and monitoring plan.

## 7. Non-Functional Requirements

- Auditability: material events, decisions, approvals, and evidence must be traceable.
- Security: secrets must never appear in prompts, logs, commits, or documentation.
- Reliability: production assets require recovery plans before activation.
- Governance: policies must be enforceable before agent execution.
- Extensibility: future agents and capabilities must be added through controlled lifecycle processes.
- Observability: meaningful actions must produce logs, status, and reviewable outcomes.
- Portability: founder-owned assets and data must not be locked behind agent-controlled accounts.

## 8. System Layers

1. Founder Interface: Founder Command Center and approval surfaces.
2. Governance Layer: Governance Core, Policy Engine, approvals, risk controls.
3. Orchestration Layer: Workflow Orchestrator and State Machine.
4. Agent Layer: Agent Registry, contracts, roles, capabilities, lifecycle.
5. Capability Layer: Capability Registry, Gap Detector, Evolution Framework.
6. Access Layer: Tool Gateway and AI Gateway.
7. Record Layer: Evidence Ledger, Decision Ledger, Asset Registry.
8. Recovery Layer: backups, rollback, monitoring, incident response.

## 9. Governance Core

The Governance Core defines mandatory rules, approval paths, autonomy limits, ownership constraints, and escalation conditions. It is the highest internal authority below the founder.

The Governance Core must prevent action when required evidence, approval, risk review, asset ownership, or recovery planning is missing.

## 10. Policy Engine

The Policy Engine evaluates proposed actions against governance rules. It returns allow, deny, require approval, require evidence, require review, or require rollback-plan outcomes.

Policies must be explicit, versioned, and auditable.

## 11. Workflow Orchestrator

The Workflow Orchestrator coordinates tasks, approvals, agent handoffs, event handling, and state transitions. Trigger.dev is the preferred first workflow engine. Temporal may be considered later if workflow durability requirements exceed Trigger.dev capabilities.

## 12. State Machine

The State Machine controls lifecycle transitions for opportunities, agents, approvals, production assets, and incidents. No workflow should rely on informal status text when a formal state is required.

## 13. Agent Registry

The Agent Registry stores approved agents, owners, responsibilities, capabilities, constraints, allowed inputs, allowed outputs, escalation rules, and activation status.

Agents cannot modify their own contract, approve themselves, or grant themselves new capabilities.

## 14. Capability Registry

The Capability Registry defines system capabilities independently from specific agents. Capabilities include purpose, risk class, dependencies, required approvals, and allowed tools.

## 15. Capability Gap Detector

The Capability Gap Detector identifies missing capabilities based on failed workflows, repeated manual work, blocked opportunities, or strategic requirements. Detection does not authorize implementation.

## 16. Agent Evolution Framework

The system may detect that a capability is missing, recommend a new agent, and draft an agent contract. It may not activate a new agent without founder approval.

New supporting agents must follow this lifecycle:

Capability Gap Detected -> Agent Proposal -> Risk Review -> Auditor Review -> Founder Approval -> Sandbox Test -> Activation Approval

## 17. Tool Gateway

The Tool Gateway is the only permitted path from agents to external tools. Agents may request tool actions; they may not directly hold credentials, bypass policy checks, or access external systems outside the gateway.

## 18. AI Gateway

The AI Gateway is the only permitted path from the system to AI providers. OpenAI, Claude, Gemini, or other providers may be supported behind the gateway. Prompts must exclude secrets and must be logged according to security and audit policy.

## 19. Evidence Ledger

The Evidence Ledger records validation material, research, measurements, test results, source references, and confidence levels. Evidence must be linked to decisions and actions.

## 20. Decision Ledger

The Decision Ledger records meaningful decisions, decision owner, evidence used, options considered, approval status, date, expected outcome, and rollback or revisit criteria.

## 21. Founder Command Center

The Founder Command Center is the founder-facing control surface for approvals, venture status, evidence review, decisions, risks, spending thresholds, agent status, and production asset health.

## 22. Asset Registry

The Asset Registry records production assets, owner, location, backup plan, rollback plan, monitoring plan, cost profile, and dependency map. No production asset is complete without these fields.

## 23. Security Architecture

Security is policy-led. Secrets are never committed, logged, documented, or sent to prompts. Credentials belong in approved secret stores controlled by the founder. Agents receive scoped capabilities, not raw credentials.

## 24. Recovery Architecture

Recovery planning is required before production activation. Each production asset must define owner, backup, rollback, monitoring, incident trigger, and escalation path.

## 25. Event Architecture

Events should represent meaningful system facts such as evidence recorded, decision proposed, approval requested, approval granted, policy denied, workflow started, state changed, asset registered, and incident opened.

Event contracts must be versioned and documented before implementation.

## 26. Database Architecture

Supabase Postgres is the preferred initial database direction. The schema must support governance, evidence, decisions, agents, capabilities, assets, workflows, state, approvals, and audit trails.

No database schema is approved until phase-level requirements and data contracts are reviewed.

## 27. Initial Agent Set

- CEO Agent: coordinates strategy, prioritization, and venture-level recommendations.
- Research Agent: gathers and structures evidence.
- Product Agent: drafts product hypotheses, validation plans, and implementation scopes.
- Risk Agent: identifies risk, controls, and required approvals.
- Auditor Agent: reviews compliance, auditability, and governance adherence.
- Tool Gateway Agent: mediates tool requests through approved gateway policies.

## 28. Development Phases

- Phase -1: Architecture Foundation.
- Phase 0: Governance Foundation.
- Phase 1: Assisted Opportunity Intake and Validation.
- Phase 2: Evidence and Decision Ledgers.
- Phase 3: Agent Registry and Capability Registry.
- Phase 4: Tool Gateway and AI Gateway.
- Phase 5: Founder Command Center.
- Phase 6: Controlled Semi-Autonomous Workflows.

Future phases require ADRs and phase specifications before implementation.

## 29. Acceptance Criteria

- Master architecture exists and is reviewed.
- ADRs define source of truth, autonomy posture, and agent evolution control.
- Governance rules are explicit.
- Initial agent contracts exist.
- State machine drafts exist.
- Evidence and decision ledger specifications exist.
- Implementation areas are present but contain no production code.

## 30. Explicit Non-Goals

- No production application code.
- No paid service installation.
- No real integrations.
- No secrets or environment values.
- No external service connection.
- No deployment automation.
- No agent self-modification.
- No direct agent access to external tools or AI providers.

## 31. Architecture Review Checklist

- Is the change consistent with founder ownership?
- Is there evidence for the proposed action?
- Has validation preceded build work?
- Are autonomy level and approval requirements explicit?
- Is tool access routed through Tool Gateway?
- Is AI access routed through AI Gateway?
- Are secrets excluded from prompts, logs, commits, and documentation?
- Is the decision auditable?
- Are asset owner, backup, rollback, and monitoring plans defined?
- Has risk review occurred where required?
- Has auditor review occurred where required?
- Is founder approval required and recorded where appropriate?

