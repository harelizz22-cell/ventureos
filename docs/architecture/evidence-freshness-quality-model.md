# Evidence Freshness And Quality Model

Parent: `docs/contracts/evidence-ledger-spec.md`

Source Of Truth: This file is the source of truth for Evidence freshness and quality architecture.

## Purpose

Define how VentureOS evaluates whether Evidence is trustworthy, current, suitable, and sufficiently corroborated for governed Decisions.

## Evidence Quality Tiers

Evidence quality tiers classify evidence strength:

- Tier 1: Primary verified source, direct observation, signed record, production record, or approved audit record.
- Tier 2: Strong internal or external source with clear provenance and reviewer validation.
- Tier 3: Secondary source, summarized research, customer signal, or interpreted operating data with clear limits.
- Tier 4: Weak, incomplete, stale, uncorroborated, or low-confidence input.
- Tier 5: Draft, unverified, AI-generated, opinion, or hypothesis support that is not Evidence until promoted.

Tier labels do not automatically approve Decisions. They inform suitability and required review.

## Source Quality

Evidence records must identify source quality:

- Primary
- Secondary
- Internal
- External
- Founder-provided
- Customer-provided
- Investor-provided
- Observed
- Estimated
- AI-generated draft
- Unknown or unverified

Unknown or unverified sources must not support high-risk Decisions without corroboration and review.

## Collection Timestamp

Evidence must record collection or capture timestamp.

Where available, Evidence should also record:

- Source publication time
- Observation time
- Review time
- Expiration time or freshness window

## Freshness Window

Freshness windows define how long Evidence remains suitable for a Decision category.

Freshness windows must consider:

- Market volatility
- Pricing volatility
- Legal or compliance sensitivity
- Customer behavior change
- Financial risk
- Operational risk
- Regulated domain sensitivity

## Expiration Model

Evidence may be:

- Current
- Aging
- Stale
- Expired
- Superseded
- Withdrawn

Expired, withdrawn, or superseded Evidence must not support new Decisions unless a governance rule explicitly allows historical context use.

## Knowledge Graph Node Freshness

Enterprise Knowledge Graph nodes used for reasoning or governed recommendations must expose freshness status from their source records where available.

Reasoning outputs must declare whether material Knowledge Graph nodes are current, aging, stale, expired, superseded, withdrawn, or unknown.

Stale, expired, superseded, withdrawn, or unknown-freshness nodes may be used as historical context only when explicitly classified and governed.

Superseded knowledge must link to the superseding source record where known.

## Corroboration Requirements

High-risk Decisions may require multiple independent Evidence records.

Corroboration requirements may vary by:

- Decision category
- Capital amount
- Regulatory sensitivity
- Autonomy level
- Production asset impact
- Customer impact
- Security impact
- Investor or funding relevance

## Stale Evidence Handling

Stale Evidence must be marked before use.

When stale Evidence is referenced:

- Decision reviewers must see stale status.
- Reasoning and recommendations must disclose freshness limits.
- Policy Engine may require updated Evidence.
- Audit must preserve that stale Evidence was considered.

## Evidence Suitability By Decision Category

Evidence suitability must be evaluated by Decision category:

- Venture validation
- Build approval
- Capital allocation
- Investment recommendation
- Funding readiness
- Investor exposure
- Autonomy promotion
- Production deployment
- Recovery action
- Legal/compliance-sensitive action

More sensitive Decisions require stronger, fresher, and better corroborated Evidence.

## AI-Generated Content

AI-generated content cannot become Evidence without promotion governance.

AI output starts as Draft, Recommendation, or Candidate Evidence and becomes Verified Evidence only through AI Output Classification and Evidence Promotion governance.

## Rule

Evidence must be classified by quality, source, timestamp, freshness, suitability, and corroboration before supporting governed Decisions.

## Placeholder Status

This is architecture documentation only. It does not define schemas, scoring formulas, databases, APIs, services, or implementation.
