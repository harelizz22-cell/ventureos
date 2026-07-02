# Consensus Engine

Parent: `docs/architecture/strategic-review-domain.md`

Source Of Truth: This file is the source of truth for Consensus Engine architecture.

## Purpose

Define how VentureOS summarizes the review process into a recommendation.

Consensus does not mean majority vote.

## Consensus Output

Consensus output must include:

- Recommended action.
- Confidence score.
- Thesis alignment.
- Opportunity score.
- Risk score.
- Evidence quality.
- Expected ROI.
- Enterprise Value impact.
- Capital required.
- Recommended stage gate.
- Dissent summary.
- Minority opinion.
- Strongest counter-argument.
- Dissent confidence.
- Founder override linkage where applicable.
- Required approvals.

## Rule

Consensus Engine does not make final decisions.

It produces governed recommendations only.

## Governance Requirements

Consensus must preserve dissent, evidence quality, approval requirements, and uncertainty. Founder or approved governance policy makes final decisions.

Consensus must not flatten minority opinions into a single aggregate score.

The strongest counter-argument must be included even when the recommendation is positive.

If Founder overrides dissent, the override must link back to the preserved dissent record.

Consensus may incorporate Reasoning Engine outputs, Enterprise Knowledge Graph context, Organizational Memory records, and Learning Engine outputs, but it must preserve their classification. Reasoning output is advisory and may not be treated as Evidence unless promoted through AI Output Classification and Evidence Promotion governance.

## Placeholder Status

This is architecture documentation only. It does not define scoring formulas, models, services, or implementation.
