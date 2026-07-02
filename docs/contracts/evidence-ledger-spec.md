# Evidence Ledger Specification

Parent: `docs/contracts/agent-contracts.md`

Source Of Truth: This file is the source of truth for Evidence Ledger contract requirements.

## Purpose

The Evidence Ledger records evidence used to evaluate opportunities, support decisions, validate assumptions, and audit meaningful action.

Evidence freshness and quality requirements are defined in `docs/architecture/evidence-freshness-quality-model.md`.

## Scope

This specification defines the documentation contract for evidence records. It does not define database schema, API endpoints, implementation code, or vendor-specific storage.

## Required Fields

- Evidence ID
- Date captured
- Title
- Source
- Source type
- Source owner or publisher
- Summary
- Claim supported or challenged
- Confidence level
- Quality assessment
- Quality tier
- Freshness status
- Freshness window
- Expiration status
- Related opportunity
- Related decision
- Reviewer
- Review status
- Timestamp

## Evidence Quality Rules

Evidence must distinguish observed facts, assumptions, interpretations, and conclusions. Weak or incomplete evidence may be recorded, but it must not be treated as validated proof.

Evidence must identify quality tier, source quality, collection timestamp, freshness status, and suitability for the Decision category where meaningful.

## Source Requirements

Evidence records must identify where the evidence came from and whether the source is primary, secondary, internal, external, estimated, or founder-provided.

## Timestamp Requirements

Evidence records must include the time they were captured or created. Time-sensitive evidence must identify when it may become stale.

Expired, withdrawn, superseded, or stale Evidence must be visibly marked before it is used for new Decisions.

## Confidence Requirements

Evidence records must assign a confidence level and explain the basis for that confidence when the evidence supports a meaningful decision.

## Auditor Review Requirements

Auditor review is required when evidence supports architecture-changing, governance-sensitive, high-risk, spending, production asset, or autonomy-expanding decisions.

## Relationship To Opportunity Validation

Opportunity validation must link to Evidence Ledger records. Build work may not proceed when validation evidence is missing or insufficient.

## Ledger Integrity Rules

Evidence Ledger, Decision Ledger, and Audit Ledger are separate architectural concerns.

Evidence must exist before Decision. Decision without Evidence is invalid.

Evidence never changes historical Decision records. If evidence changes later, a new evidence record and follow-up decision are required.

When Knowledge is referenced as Evidence for a Decision, the referenced Knowledge version must be immutable or snapshot-pinned.

Evidence must never depend on mutable current-state content.

Observability signals may be promoted to Evidence for Decisions only through a governed promotion process. Raw telemetry must not automatically become Evidence.

## AI Evidence Promotion Queue

AI-generated Candidate Evidence must pass through a governed promotion queue before it may become Verified Evidence.

Candidate Evidence is never treated as Verified Evidence.

Promotion queue records must preserve source output, source classification, source citations, scope, reviewer, delegation authority, review status, and promotion, denial, or deferral reason.

Batch promotion is allowed only when policy permits compatible Evidence category, source type, scope, risk, and decision category. Batch promotion must not hide individual evidence quality, freshness, source, uncertainty, or denial reasons.

Denied promotion and deferred promotion must create Audit records.

Promotion backlog must be visible, prioritized, and escalated where delay affects governed Decisions.

## Reasoning-To-Evidence Enforcement

Evidence Ledger must reject direct Reasoning Engine outputs.

Reasoning output may enter Evidence Ledger only after a promotion record exists, source classification is present, and the required promotion path has approved the write.

Reasoning output without promotion remains reasoning, not Evidence.

AI-generated content cannot become Evidence without promotion governance. AI output follows Draft -> Recommendation -> Candidate Evidence -> Verified Evidence.

## Future Database Mapping Note

Future database design must map these required fields without weakening evidence quality, source, timestamp, confidence, or audit requirements.

## Future API Contract Note

Future API contracts must preserve the same required fields, evidence quality rules, source requirements, timestamp requirements, confidence requirements, and review behavior defined here.
