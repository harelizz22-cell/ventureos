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

## Runtime Model

Everything meaningful emits events. Future systems must subscribe to events instead of tightly coupling services.

Every Capability must contribute toward measurable business outcomes. Every Workflow must exist because it creates business value.

## Value Model

Founder Decision -> Workflow -> Capability -> Execution -> Cost -> Revenue -> Profit -> Enterprise Value

## Strategic Thinking Model

Thesis -> Hypothesis -> Validation -> Opportunity Score -> Capital Allocation -> Execution -> Outcome -> Learning -> Enterprise Value

No Venture may move from idea to validation without an approved hypothesis.

No Venture, external investment, acquisition, or capital allocation may proceed without Thesis alignment review.

Portfolio Diversification identifies concentration risk before capital or investment recommendations.

Learning converts outcomes into evidence-backed, auditable reusable knowledge.

## Product Entry

The primary product entry is the Founder Operating Console. The primary screen is the Founder Command Center.

The console must answer within five seconds: Where is my money? Where is my risk? Where is my growth? What requires my approval? What is blocked? What changed today? What is the expected outcome?

## Long-Term Scale Target

VentureOS must be able to manage multiple Organizations, multiple Portfolios, hundreds of Ventures, thousands of Capabilities, and millions of Events without architectural redesign.
