# ADR-066: Global Search

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Global Search decision.

## Status

Accepted

## Context

Enterprise-scale VentureOS needs unified search across Evidence, Decisions, Ventures, Organizations, Workflows, Executions, Assets, ADRs, Playbooks, Knowledge, and Organizational Memory.

## Decision

VentureOS adopts Global Search as a policy-enforced enterprise search architecture that respects tenant, Venture, role, classification, Evidence, compliance, and source-of-truth boundaries.

## Alternatives

- Search each document or Domain separately.
- Create search without Policy Engine enforcement.
- Expose metadata or snippets outside authorized scope.

## Rationale

Unified search improves usability and continuity, but only if it preserves enterprise isolation.

## Risks

- Search may leak existence signals.
- Search ranking may blur active architecture and candidate material.
- Search may expose unauthorized snippets or metadata.

## Consequences

- Search results must be permission-filtered.
- Search must preserve classification and Evidence status.
- Search must not expose unauthorized content or metadata.

## Enforcement

Global Search must always respect Policy Engine permissions.
