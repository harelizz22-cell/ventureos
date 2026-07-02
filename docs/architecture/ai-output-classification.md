# AI Output Classification

Parent: `docs/architecture/ai-gateway.md`

Source Of Truth: This file is the source of truth for AI output classification architecture.

## Purpose

Define how VentureOS classifies AI-generated outputs before they may influence Decisions, Evidence, recommendations, or execution.

## Lifecycle

AI output follows this lifecycle:

Draft -> Recommendation -> Candidate Evidence -> Verified Evidence

## Draft

Draft output is unverified working material.

Draft output may help prepare research, summaries, options, and review material, but it is not Evidence.

## Recommendation

Recommendation output proposes a course of action, interpretation, risk, option, or next step.

Recommendation output must cite sources, assumptions, confidence, uncertainty, and limitations where meaningful.

Recommendation output is not Evidence.

## Candidate Evidence

Candidate Evidence is AI output proposed for review as possible Evidence.

Candidate Evidence requires source review, confidence assessment, evidence quality evaluation, and governance approval before it can become Verified Evidence.

## Verified Evidence

Verified Evidence is promoted through governance and recorded according to Evidence Ledger requirements.

AI output must never enter Evidence Ledger directly without promotion governance.

## Required AI Output Metadata

AI output must be traceable where possible to:

- Model
- Provider
- Prompt
- Context
- Source inputs
- Tool outputs
- Actor
- Time
- Scope
- Confidence
- Uncertainty
- Limitations

## Hallucination Risk Mitigation

AI hallucination risk must be explicitly mitigated through:

- Source citation
- Source review
- Confidence marking
- Uncertainty marking
- Limitations disclosure
- Corroboration where required
- Evidence Promotion governance

## Rule

AI output is never Evidence by default.

Promotion to Evidence requires governance.

Candidate Evidence is never treated as Verified Evidence.

## Evidence Promotion Queue Governance

Candidate Evidence enters a promotion queue before it may become Verified Evidence.

Promotion queue records must preserve:

- Candidate Evidence identifier.
- Source AI output classification.
- Source inputs and citations.
- Scope.
- Actor or requesting component.
- Delegated reviewer where allowed.
- Batch membership where applicable.
- Review status.
- Promotion, denial, or deferral reason.
- Audit link.

Delegation rules:

- Delegated promotion review must be explicitly authorized by policy.
- Delegation must preserve reviewer identity, scope, evidence category, and approval authority.
- Capital-sensitive, compliance-sensitive, autonomy-expanding, architecture-changing, or high-risk Evidence may require Founder, auditor, compliance, or domain reviewer approval.

Batch promotion constraints:

- Batch promotion may only group similar Evidence with compatible source type, scope, risk, and decision category.
- Batch promotion must not hide individual source quality, freshness, uncertainty, or denial reasons.
- Batch size must be bounded by policy and reviewer capacity.

Throughput expectations must be visible so Candidate Evidence does not silently accumulate. Backlog handling may include prioritization, escalation, deferral, expiry, or denial.

Denied promotion must create an Audit record with denial reason and reviewer.

Deferred promotion must create an Audit record with deferral reason, next review condition, and owner.

## Reasoning-To-Evidence Runtime Enforcement

Evidence Ledger must reject direct Reasoning Engine outputs.

Reasoning output requires a promotion record before it may become Candidate Evidence or Verified Evidence.

Source classification is required before any Evidence write.

Promotion path must be present before Evidence Ledger write.

## Placeholder Status

This is architecture documentation only. It does not define model providers, prompts, classifiers, services, schemas, integrations, or implementation.
