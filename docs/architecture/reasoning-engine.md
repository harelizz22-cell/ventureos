# Reasoning Engine

Parent: `docs/architecture/knowledge-domain.md`

Source Of Truth: This file is the source of truth for Reasoning Engine architecture.

## Purpose

Reasoning Engine is the architecture component that derives conclusions from approved knowledge, Organizational Memory, Evidence, and current context.

It produces explainable reasoning outputs and recommendations only. It does not create final Decisions.

## Supports

Reasoning Engine may support:

- Pattern detection
- Contradiction detection
- Similarity analysis
- Historical comparison
- Opportunity reasoning
- Risk reasoning
- Investment reasoning
- Strategy reasoning
- Portfolio reasoning
- Capital allocation reasoning
- Hypothesis challenge
- Thesis alignment reasoning

## Required Citations

Every reasoning output must cite:

- Source knowledge
- Evidence records
- Assumptions
- Confidence
- Uncertainty
- Dissent where relevant

Reasoning without cited sources, assumptions, confidence, and uncertainty is not valid for governed review.

## Evidence Boundary

Reasoning output may not become Evidence automatically.

Reasoning output may become Candidate Evidence only through AI Output Classification and Evidence Promotion governance.

The required lifecycle remains:

Draft -> Recommendation -> Candidate Evidence -> Verified Evidence

AI Output Classification requirements are defined in `docs/architecture/ai-output-classification.md`.

AI Model Registry requirements are defined in `docs/architecture/ai-model-registry.md`.

Evidence Ledger must reject direct Reasoning outputs. Reasoning output requires source classification and a promotion record before any Evidence write.

## Governance Requirements

- Reasoning outputs must preserve scope and actor context.
- Reasoning outputs must preserve Organization, Portfolio, Venture, tenant, Knowledge, Memory, Evidence, and AI context isolation.
- Reasoning must distinguish facts, Evidence, Decisions, assumptions, forecasts, opinions, and learning.
- Reasoning must surface contradictions rather than hide them.
- Reasoning must preserve material dissent where relevant.
- Reasoning output must identify limitations and hallucination risk where AI-generated.
- Reasoning output must record which approved model produced the recommendation where AI generated it.
- Reasoning output must include freshness status for each material Knowledge Graph node, Evidence record, Memory record, or Learning record used.
- Reasoning cannot approve Venture validation, capital allocation, investment, acquisition, funding, execution, or strategy.
- Founder or approved governance policy remains final decision authority.
- Cross-Venture reasoning must follow Cross-Venture Intelligence rules.
- Cross-Organization reasoning is forbidden unless explicitly governed.

## Relationship To Other Components

- Knowledge Domain owns knowledge assets and retrieval capabilities.
- Enterprise Knowledge Graph provides structured relationships across approved knowledge and architecture entities.
- Organizational Memory provides durable history.
- Learning Engine provides evidence-backed learnings from outcomes.
- Reasoning Engine consumes approved knowledge and memory to produce reasoning outputs.
- Strategic Review Domain may use Reasoning Engine outputs as inputs to Debate, Consensus, and Investment Memo artifacts.

## Reasoning Input Freshness

Reasoning Engine must evaluate input freshness before producing governed recommendations.

Freshness status must be included in every reasoning output.

Freshness status must identify:

- Current inputs.
- Aging inputs.
- Stale inputs.
- Expired inputs.
- Superseded inputs.
- Withdrawn inputs.
- Unknown freshness inputs.

Knowledge Graph node freshness must be read from Enterprise Knowledge Graph source records and Evidence freshness metadata where available.

Stale node declaration is required when a material reasoning input is stale, expired, superseded, withdrawn, or missing freshness metadata.

Superseded knowledge handling must prefer the latest approved source record unless historical context is explicitly requested and classified.

Reasoning output must not hide stale or superseded inputs behind an aggregate confidence score.

## VC Pattern Recognition Readiness

VentureOS should learn from professional venture capital pattern recognition as architecture readiness only.

Future governed reasoning may help detect:

- Repeated market patterns
- Repeated pricing failures
- Repeated customer acquisition cost failures
- Repeated Founder override outcomes
- Repeated Thesis violations
- Repeated successful GTM patterns
- Repeated regulatory blockers
- Repeated capital inefficiency patterns
- Repeated execution failure modes
- Repeatable playbooks

This is not active implementation. It does not define models, prompts, ranking logic, automation, services, or integrations.

## Rule

Reasoning Engine does not create final Decisions.

It produces explainable reasoning outputs and recommendations only.

Reasoning Engine may only use models approved for reasoning workloads by AI Model Registry and Policy Engine.

## Placeholder Status

This is architecture documentation only. It does not define inference models, prompts, vector search, graph algorithms, services, integrations, UI, or implementation.
