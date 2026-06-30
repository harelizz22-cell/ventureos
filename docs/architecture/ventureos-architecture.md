# VentureOS Architecture

Parent: `docs/project/ventureos-system-bible.md`

Source Of Truth: This file is the technical architecture index for VentureOS.

## Purpose

This document identifies the source of truth for each technical architecture concern. It does not replace concern-specific architecture documents.

## Official Definitions

These definitions are architectural vocabulary. All future documents must use them consistently.

- Capability: A durable system ability owned by a Domain and invokable through governed execution. A Capability is independent of any specific implementation mechanism.
- Domain: A business area that owns Capabilities, Policies, Events, Workflows, Data, Interfaces, and future implementations.
- Workflow: A structured sequence of steps that coordinates a Capability or related Capabilities toward an outcome.
- Execution: A governed runtime attempt to perform a Workflow or invoke a Capability through an implementation mechanism.
- Evidence: Recorded support, proof, observation, source material, or validation input used before Decisions.
- Decision: A recorded choice made by an authorized actor based on Evidence and applicable governance.
- Audit: Append-only record of meaningful actions, state changes, approvals, denials, executions, events, and governance-relevant history.
- Event: A meaningful runtime fact emitted by VentureOS for auditability, coordination, observability, and decoupled subscription.
- Autonomy Level: A configured runtime permission level that defines what the system may observe, recommend, request, or execute.
- Execution Orchestrator: The architecture component that owns execution flow, capability invocation, governance enforcement, approval waiting, retries, timeouts, failure containment, event coordination, recovery triggering, and execution state tracking.
- Runtime Kernel: The execution foundation that runs the system by coordinating policy, execution, scheduling, state, approvals, events, recovery, and resources without making business decisions.
- Execution API: The single governed entry point for all Capability execution requests.
- Strategic Review Domain: The Domain responsible for structured business review before VentureOS recommends building, investing, funding, scaling, pausing, or exiting.
- Business Outcome: A measurable result that contributes to revenue, profit, growth, risk reduction, operational quality, or enterprise value.
- Enterprise Value: The long-term measurable value of a company or portfolio created through revenue, profit, assets, defensibility, growth, and operational maturity.
- Capital: Financial and economic resources available for allocation across Ventures, Capabilities, investments, infrastructure, tools, and operations.
- Capital Allocation: The governed recommendation or decision process for assigning capital to the highest expected Enterprise Value use.
- Investment: A governed allocation of capital into an internal Venture, external startup, acquisition, partnership, capability, infrastructure, or growth opportunity.
- Opportunity Score: An evidence-linked metric used to compare opportunities by market size, competition, execution complexity, founder confidence, evidence quality, expected revenue, expected profit, strategic alignment, risk, expected ROI, time to revenue, and capital required.
- Thesis: The Founder and Organization investment/build strategy defining preferred and excluded markets, business models, geography, risk tolerance, capital range, return expectations, time horizon, and strategic constraints.
- Hypothesis: An explicit, testable business assumption for a Venture before validation, including problem, audience, solution, assumptions, success criteria, kill criteria, validation plan, expected ROI, and Thesis alignment.
- Portfolio Diversification: The architecture concern that monitors concentration risk across sector, geography, stage, technology, capital, providers, revenue models, and correlated risks.
- Learning: Evidence-backed conversion of outcomes into reusable knowledge for future strategy, scoring, recommendations, and governance.
- Funding Round: A future governed planning object for capital target, milestone funding plan, investor commitments, readiness status, and evidence-based release recommendations.
- Investment Marketplace: A future compliance-gated capability for exposing selected, reviewed Venture opportunities to qualified investors through evidence-based dossiers.
- Investment Readiness: A future review gate that determines whether a Venture is mature enough to be shown to investors.
- Investment Dossier: A future investor-facing explanation package that distinguishes assumptions, evidence, forecasts, and confirmed facts.
- Compliance Gate: An enforceable runtime gate for restricted capability categories, legal approval records, investment marketplace gating, and regulated domain gating.
- Capital Reservation: A governed record reserving capital for a proposed allocation without moving money or executing an investment.
- Learning Quarantine: A governed state that prevents disputed, quarantined, or withdrawn learning from silently influencing future recommendations while preserving audit.

## Current Architecture Posture

VentureOS is an Enterprise Value-first Company Operating System, not an AI Operating System. AI is an execution mechanism, not the identity of the system.

VentureOS exists to maximize long-term Enterprise Value while preserving Founder control, governance, transparency, and capital discipline. Revenue is an important KPI, but Enterprise Value is the primary objective.

VentureOS is outcome-driven, Portfolio-first, and capability-first, not task-driven, workflow-driven, or agent-driven. A single venture is simply a portfolio containing one venture. Agents are implementation details.

The architecture hierarchy is:

Founder -> Organization -> Portfolio -> Venture -> Domain -> Capability -> Workflow -> Execution -> Evidence -> Decision -> Audit

Authority hierarchy:

Founder -> Organization -> Portfolio -> Venture

Business hierarchy begins at Organization. Founder remains the highest authority but is not a business entity.

The architecture is configured for Autonomy Level 1: Assisted Mode and must remain autonomy-ready.

The long-term architecture must support multiple Organizations, multiple Portfolios, hundreds of Ventures, thousands of Capabilities, and millions of Events without architectural redesign.

VentureOS measures success by business outcomes, not technical activity. Every Capability must contribute toward measurable business outcomes. Every Workflow must exist because it creates business value. Every autonomous action must be traceable to a measurable objective.

VentureOS does not measure success by revenue alone. Revenue matters because it contributes to Enterprise Value.

VentureOS is designed to become a venture studio, capital allocation system, and future investor marketplace because it combines Thesis, Hypothesis, Evidence, Policy, Audit, Funding, Investment Readiness, Investment Dossiers, and governed execution into one architecture. Future investor participation is not enabled in MVP and remains compliance-gated.

VentureOS must not claim it can legally raise funds, sell securities, hold investor money, or execute investments without the appropriate legal entity, licensing, jurisdictional review, and compliance framework.

## Technical Source Of Truth Map

- Architecture Principles: `docs/architecture/architecture-principles.md`
- Phase 2 Architecture Blueprint: `docs/phases/phase-2-architecture-blueprint.md`
- Context map: `docs/architecture/context-map.md`
- Organization and Portfolio model: `docs/architecture/organization-portfolio-model.md`
- Domain model: `docs/architecture/domain-model.md`
- Business Intelligence Domain: `docs/architecture/business-intelligence.md`
- Strategic Review Domain: `docs/architecture/strategic-review-domain.md`
- Knowledge Domain: `docs/architecture/knowledge-domain.md`
- Identity Domain: `docs/architecture/identity-domain.md`
- Resource Domain: `docs/architecture/resource-domain.md`
- System layers: `docs/architecture/system-layers.md`
- System components: `docs/architecture/system-components.md`
- Event architecture: `docs/architecture/event-architecture.md`
- Database architecture: `docs/architecture/database-architecture.md`
- Asset Registry: `docs/architecture/asset-registry.md`
- Venture Timeline: `docs/architecture/venture-timeline.md`
- Venture Health Model: `docs/architecture/venture-health-model.md`
- Venture Digital Twin: `docs/architecture/venture-digital-twin.md`
- Value Graph: `docs/architecture/value-graph.md`
- Founder Decision Graph: `docs/architecture/founder-decision-graph.md`
- Revenue KPIs: `docs/architecture/revenue-kpis.md`
- Enterprise Value Engine: `docs/architecture/enterprise-value-engine.md`
- Capital Allocation Engine: `docs/architecture/capital-allocation-engine.md`
- Investment Engine: `docs/architecture/investment-engine.md`
- Thesis Engine: `docs/architecture/thesis-engine.md`
- Portfolio Diversification: `docs/architecture/portfolio-diversification.md`
- Learning Engine: `docs/architecture/learning-engine.md`
- Hypothesis Engine: `docs/architecture/hypothesis-engine.md`
- Funding Engine: `docs/architecture/funding-engine.md`
- Investment Marketplace: `docs/architecture/investment-marketplace.md`
- Investor Intelligence: `docs/architecture/investor-intelligence.md`
- Investment Readiness: `docs/architecture/investment-readiness.md`
- Investment Dossier: `docs/architecture/investment-dossier.md`
- Syndicated Funding Model: `docs/architecture/syndicated-funding-model.md`
- Milestone Capital Release: `docs/architecture/milestone-capital-release.md`
- Opportunity Engine: `docs/architecture/opportunity-engine.md`
- Opportunity Score: `docs/architecture/opportunity-score.md`
- Stage Gate Investment Model: `docs/architecture/stage-gate-investment-model.md`
- Capital Governance: `docs/governance/capital-governance.md`
- Cost Governance: `docs/governance/cost-governance.md`
- Investor Marketplace Compliance: `docs/governance/investor-marketplace-compliance.md`
- Runtime behavior: `docs/runtime/`
- Runtime Kernel: `docs/architecture/runtime-kernel.md`
- Execution API: `docs/architecture/execution-api.md`
- Execution Scheduler: `docs/architecture/execution-scheduler.md`
- Resource Coordinator: `docs/architecture/resource-coordinator.md`
- Tool Gateway: `docs/architecture/tool-gateway.md`
- AI Gateway: `docs/architecture/ai-gateway.md`
- Execution Orchestrator: `docs/architecture/execution-orchestrator.md`
- Workflow Orchestrator compatibility note: `docs/architecture/workflow-orchestrator.md`
- Policy Engine: `docs/architecture/policy-engine.md`
- State machines: `docs/architecture/state-machines.md`
- Capability Registry: `docs/architecture/capability-registry.md` (primary)
- Agent Registry: `docs/architecture/agent-registry.md` (secondary)
- Agent evolution: `docs/architecture/agent-evolution.md`
- Founder Command Center: `docs/architecture/founder-command-center.md`
- Observability: `docs/architecture/observability.md`
- Dynamic Review Council: `docs/architecture/dynamic-review-council.md`
- Debate Engine: `docs/architecture/debate-engine.md`
- Consensus Engine: `docs/architecture/consensus-engine.md`
- Investment Memo Generator: `docs/architecture/investment-memo-generator.md`

## Architecture Rule

Technical implementation work must trace to this architecture index, an accepted ADR, and an active phase specification.

Phase 2 has started with `docs/architecture/architecture-principles.md` as the official non-negotiable architecture principles document.

The next Phase 2 workstream is Execution Orchestrator Decomposition.

Implementation may be performed by an AI Agent, human, external API, internal service, or future execution engine.

Execution Orchestrator is decomposed under VentureOS Runtime Kernel. Runtime Kernel does not make business decisions.

All Capability execution requests must enter through Execution API.

Strategic Review Domain owns structured opportunity review. Dynamic Review Council provides multi-perspective review. Debate and dissent are first-class architecture concepts.

Investment Memo is the formal internal review artifact before major capital decisions.

Every future capability must be multi-venture aware and must identify its owning Domain.

Every Capability must contribute toward measurable business outcomes. Every Workflow must exist because it creates business value. Every autonomous action must be traceable to a measurable objective.

Every Capital allocation and investment recommendation must include Evidence, governance evaluation, expected ROI, risk, approval requirements, and expected Enterprise Value impact.

No Venture may move from idea to validation without an approved hypothesis.

No Venture, external investment, acquisition, or capital allocation may proceed without Thesis alignment review.

Learning updates must be evidence-backed and auditable.

VentureOS must not autonomously transfer money or execute investments.

Future Funding Engine, Investment Marketplace, Investor Intelligence, Investment Readiness, Investment Dossier, Syndicated Funding Model, and Milestone Capital Release are future-phase, governance-gated, compliance-gated, evidence-based architecture concerns. They are not enabled in MVP and do not authorize regulated financial activity.

No Venture may be exposed to investors before passing Investment Readiness review.

Investment content must distinguish assumptions, evidence, forecasts, and confirmed facts. No guaranteed return language is allowed.

Phase 2 Architecture Blueprint must close critical runtime architecture gaps before system implementation. Claude Red Team Architecture Review is input, not Source of Truth.

AI output must follow Draft -> Recommendation -> Candidate Evidence -> Verified Evidence. AI output must never enter Evidence Ledger directly without promotion governance.

Policy evaluation must preserve policy version or policy snapshot used.

Compliance Gate, Capital Reservation, Learning Quarantine, Event Replay, Cross-Venture Query Governance, Multi-Tenancy Isolation, Recovery Governance, and Agent Evolution Governance must be defined before related implementation begins.

All execution paths must pass through the Policy Engine. No Capability, Agent, Workflow, Tool, Service, or External Provider may self-approve execution.

If the Policy Engine is unavailable, VentureOS must fail closed. No execution is permitted while governance is unavailable.

Evidence Ledger, Decision Ledger, and Audit Ledger are three separate architectural concerns. Evidence must exist before Decision. Decision without Evidence is invalid. Audit is append-only. Audit entries cannot be edited. Evidence never changes historical Decision records.
