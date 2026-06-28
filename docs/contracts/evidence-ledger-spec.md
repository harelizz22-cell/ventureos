# Evidence Ledger Specification

Parent: `docs/contracts/agent-contracts.md`

Source Of Truth: This file is the source of truth for Evidence Ledger contract requirements.

## Purpose

The Evidence Ledger records evidence used to evaluate opportunities, support decisions, validate assumptions, and audit meaningful action.

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
- Related opportunity
- Related decision
- Reviewer
- Review status
- Timestamp

## Evidence Quality Rules

Evidence must distinguish observed facts, assumptions, interpretations, and conclusions. Weak or incomplete evidence may be recorded, but it must not be treated as validated proof.

## Source Requirements

Evidence records must identify where the evidence came from and whether the source is primary, secondary, internal, external, estimated, or founder-provided.

## Timestamp Requirements

Evidence records must include the time they were captured or created. Time-sensitive evidence must identify when it may become stale.

## Confidence Requirements

Evidence records must assign a confidence level and explain the basis for that confidence when the evidence supports a meaningful decision.

## Auditor Review Requirements

Auditor review is required when evidence supports architecture-changing, governance-sensitive, high-risk, spending, production asset, or autonomy-expanding decisions.

## Relationship To Opportunity Validation

Opportunity validation must link to Evidence Ledger records. Build work may not proceed when validation evidence is missing or insufficient.

## Future Database Mapping Note

Future database design must map these required fields without weakening evidence quality, source, timestamp, confidence, or audit requirements.

## Future API Contract Note

Future API contracts must preserve the same required fields, evidence quality rules, source requirements, timestamp requirements, confidence requirements, and review behavior defined here.

