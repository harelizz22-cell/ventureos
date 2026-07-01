# VentureOS Context Map

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the first architecture document every new contributor should read.

## Purpose

Explain the VentureOS architecture in one page.

## Core Identity

VentureOS is an Enterprise Value-first Company Operating System. It exists to maximize long-term Enterprise Value while preserving Founder control, governance, transparency, and capital discipline. Revenue is an important KPI, but Enterprise Value is the primary objective.

AI is not the product. AI is one execution option.

VentureOS is outcome-driven, Portfolio-first, and capability-first. A single venture is a portfolio containing one venture.

## Architecture Hierarchy

Founder
-> Organization
-> Portfolio
-> Venture
-> Domain
-> Capability
-> Workflow
-> Execution
-> Evidence
-> Decision
-> Audit

## Execution Model

Capabilities are invoked through the Execution Orchestrator. Implementation may be AI, human, API, internal service, or future engine.

## Domain Interaction Model

Domains never share state directly.

Allowed interaction channels are governed Capability invocation through the Execution Orchestrator and Policy Engine, and Published Events through Event Architecture.

No Domain may read or write another Domain's database, tables, or in-memory state directly.

Domains may only be added to this Context Map after their Domain Declaration is accepted.

## Enterprise Scale Model

Organization is the primary tenant boundary.

Multi-Tenancy Architecture, Data Ownership Model, Enterprise Isolation, Enterprise Identity Model, Cross-Venture Intelligence, and Global Search define how VentureOS scales across multiple Organizations, Portfolios, Ventures, users, Agents, Capabilities, Knowledge, runtime contexts, Events, memory, search, analytics, and AI context.

No Organization may access another Organization's information unless explicitly governed.

Raw Venture data must not leak between Ventures unless Policy Engine explicitly allows governed aggregation, comparison, search, reasoning, or shared learning.

## Runtime Model

Everything meaningful emits events. Future systems must subscribe to events instead of tightly coupling services.

Every Capability must contribute toward measurable business outcomes. Every Workflow must exist because it creates business value.

## Value Model

Founder Decision -> Workflow -> Capability -> Execution -> Cost -> Revenue -> Profit -> Enterprise Value

## Capital Governance Model

Capital Allocation recommendation -> Treasury reservation -> Policy Engine evaluation -> Founder or governed approval -> Capital Lifecycle transition -> Milestone Funding release -> Spend verification -> Audit

Treasury Domain protects, reserves, releases, tracks, and reconciles capital. It does not evaluate ideas, create strategy, or bypass Policy Engine.

No money can move without Policy Engine evaluation. No capital can be allocated twice. Every dollar has a lifecycle.

## Strategic Thinking Model

Thesis -> Hypothesis -> Validation -> Opportunity Score -> Capital Allocation -> Execution -> Outcome -> Learning -> Enterprise Value

No Venture may move from idea to validation without an approved hypothesis.

No Venture, external investment, acquisition, or capital allocation may proceed without Thesis alignment review.

Portfolio Diversification identifies concentration risk before capital or investment recommendations.

Learning converts outcomes into evidence-backed, auditable reusable knowledge.

## Knowledge, Memory, And Reasoning Model

Knowledge Domain owns knowledge assets and retrieval capabilities.

Organizational Memory preserves what happened and what VentureOS remembers. Enterprise Knowledge Graph connects approved facts, Evidence, Decisions, Ventures, Markets, outcomes, and related entities. Learning Engine converts outcomes into reusable learning. Reasoning Engine infers from approved knowledge, memory, Evidence, and current context.

Reasoning outputs are recommendations only. They do not become Evidence automatically and may become Candidate Evidence only through AI Output Classification and Evidence Promotion governance.

## Future Investor Marketplace Model

Opportunity -> Investment Readiness -> Investment Dossier -> Compliance Gate -> Investor Marketplace -> Funding Round -> Milestone Capital Release -> Outcome Tracking

This is future-phase architecture only. It is governance-gated, compliance-gated, evidence-based, not enabled in MVP, and not autonomous money movement.

No Venture may be exposed to investors before passing Investment Readiness review.

The future marketplace must not sell securities, process investments, hold investor money, or claim legal fundraising authority without approved legal/compliance structure.

## Product Entry

The primary product entry is the Founder Operating Console. The primary screen is the Founder Command Center.

The console must answer within five seconds: Where is my money? Where is my risk? Where is my growth? What requires my approval? What is blocked? What changed today? What is the expected outcome?

## Long-Term Scale Target

VentureOS must be able to manage multiple Organizations, multiple Portfolios, hundreds of Ventures, thousands of Capabilities, and millions of Events without architectural redesign.
