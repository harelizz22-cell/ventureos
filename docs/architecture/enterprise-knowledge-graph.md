# Enterprise Knowledge Graph

Parent: `docs/architecture/knowledge-domain.md`

Source Of Truth: This file is the source of truth for Enterprise Knowledge Graph architecture.

## Purpose

The Enterprise Knowledge Graph is the structured relationship layer of VentureOS.

It connects approved knowledge, Evidence, Decisions, Ventures, Markets, outcomes, risks, and architecture entities so VentureOS can reason across the enterprise without turning knowledge into an ungoverned data dump.

## Connected Entities

The Enterprise Knowledge Graph stores and connects approved records about:

- Founder
- Organization
- Portfolio
- Venture
- Domain
- Capability
- Workflow
- Execution
- Evidence
- Decision
- Audit
- Hypothesis
- Thesis
- Customer
- Market
- Competitor
- Investor
- Investment
- Funding Round
- Asset
- Cost
- Revenue
- Learning
- Risk
- Exit
- Acquisition
- Playbook

## Knowledge Classification

The graph must distinguish:

- Fact
- Evidence
- Decision
- Assumption
- Forecast
- Opinion
- Learning

Classification must be explicit so forecasts are not treated as facts, opinions are not treated as Evidence, and AI reasoning does not become Evidence without promotion governance.

## Source Record Rule

The Enterprise Knowledge Graph is not allowed to become an ungoverned data dump.

All graph entries must trace back to approved source records, including Evidence records, Decision records, Audit records, approved Knowledge assets, Venture records, Portfolio records, or other governed source-of-truth documents.

Graph relationships may improve discoverability and reasoning, but they do not replace source records.

Graph entries referenced as Evidence must trace to Evidence records that satisfy freshness, quality, source, timestamp, suitability, and corroboration requirements.

## Governance Requirements

- Every graph entry must identify source, scope, classification, and provenance.
- Every graph relationship must be explainable from approved source records.
- Evidence-linked graph entries must preserve Evidence source and version where meaningful.
- Evidence-linked graph entries must preserve freshness and quality status where meaningful.
- Decision-linked graph entries must preserve Decision authority and audit trail.
- Cross-venture graph traversal must follow Cross-Venture Query Governance.
- Cross-tenant graph traversal is forbidden unless explicitly governed.
- Graph access must preserve Data Ownership Model, Enterprise Isolation, and Policy Engine authorization.
- Regulated, investor, medical, financial, biotech, security, and legal knowledge must remain compliance-gated where required.

## Relationship To Other Components

- Knowledge Domain owns knowledge assets and retrieval capabilities.
- Enterprise Knowledge Graph owns the relationship model across approved knowledge and architecture entities.
- Organizational Memory preserves durable history.
- Learning Engine converts outcomes into reusable learning.
- Reasoning Engine consumes approved knowledge, memory, Evidence, and current context to produce explainable reasoning outputs.

## VC Pattern Recognition Readiness

VentureOS should learn from professional venture capital pattern recognition as architecture readiness only.

Future governed reasoning may detect:

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

This is not active implementation. It does not define models, graph storage, ranking logic, automation, or runtime services.

## Rule

Enterprise Knowledge Graph strengthens long-term organizational intelligence, but it does not make autonomous decisions, approve capital allocation, replace Evidence, or rewrite historical records.

## Placeholder Status

This is architecture documentation only. It does not define graph database technology, schemas, embeddings, services, integrations, automation, UI, or implementation.
