# ADR-054: Evidence Freshness And Quality Model

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Evidence Freshness and Quality Model decision.

## Status

Accepted

## Context

VentureOS requires Evidence before meaningful Decisions, but Evidence also needs freshness, quality, source, corroboration, and suitability rules so stale or weak information does not support high-risk Decisions.

## Decision

VentureOS adopts the Evidence Freshness and Quality Model for evidence quality tiers, source quality, collection timestamp, freshness windows, expiration states, corroboration requirements, stale evidence handling, and suitability by Decision category.

## Alternatives considered

- Treat all Evidence records as equally suitable.
- Let reviewers judge freshness informally.
- Allow AI-generated content into Evidence without promotion governance.

## Rationale

Evidence quality and freshness rules preserve Decision quality, auditability, and governance across validation, capital, autonomy, investor, recovery, and production-sensitive decisions.

## Risks

- Quality tiers may be misused as automatic approval.
- Freshness windows may need category-specific refinement.
- Evidence may be blocked until corroboration rules are clear.

## Consequences

- Evidence must identify quality, source, timestamp, freshness, suitability, and corroboration where meaningful.
- Stale or expired Evidence must be visible before Decision use.
- AI-generated content cannot become Evidence without promotion governance.

## Enforcement

Evidence supporting governed Decisions must satisfy the freshness and quality requirements applicable to its Decision category.
