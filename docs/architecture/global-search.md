# Global Search

Parent: `docs/architecture/knowledge-domain.md`

Source Of Truth: This file is the source of truth for Global Search architecture.

## Purpose

Define unified enterprise search across VentureOS while preserving Policy Engine permissions, tenant isolation, scope, source-of-truth boundaries, and auditability.

## Searchable Objects

Global Search must understand:

- Evidence
- Decisions
- Ventures
- Organizations
- Workflows
- Executions
- Assets
- ADRs
- Playbooks
- Knowledge
- Organizational Memory

## Permission Model

Search must always respect Policy Engine permissions.

Search results must be filtered by Organization, Portfolio, Venture, Domain, Capability, role, actor, classification, Evidence status, and compliance sensitivity where required.

## Tenant And Venture Isolation

Search must not reveal the existence, title, summary, metadata, snippet, or content of records outside authorized scope.

Cross-Venture search requires explicit policy authorization.

Cross-Organization search is forbidden unless explicitly governed.

## Source Classification

Search results must preserve classification:

- Fact
- Evidence
- Decision
- Assumption
- Forecast
- Opinion
- Learning
- AI Output

Search relevance must not blur classification or Evidence status.

## Knowledge And Memory Search

Knowledge and Organizational Memory search must preserve source, scope, provenance, freshness, and audit references where meaningful.

## Architecture And ADR Search

Architecture and ADR search must respect source-of-truth hierarchy and must not treat superseded or candidate material as active architecture.

## Audit Requirements

Search activity must be auditable where meaningful, especially for sensitive data, regulated domains, investor-related material, cross-Venture queries, and future customer contexts.

## Rule

Global Search must always respect Policy Engine permissions and must not leak unauthorized tenant, Venture, Knowledge, Memory, Evidence, Decision, Asset, or Audit data.

## Placeholder Status

This is architecture documentation only. It does not define search providers, indexes, embeddings, ranking algorithms, APIs, services, storage, or implementation.
