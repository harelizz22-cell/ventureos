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

## Placeholder Status

This is architecture documentation only. It does not define model providers, prompts, classifiers, services, schemas, integrations, or implementation.
