# Investment Memo Generator

Parent: `docs/architecture/strategic-review-domain.md`

Source Of Truth: This file is the source of truth for Investment Memo Generator architecture.

## Purpose

Define a professional investment memo similar in structure to venture capital investment committee memos.

The memo format uses professional venture capital operating patterns as architectural inspiration only. VentureOS does not copy any VC firm.

## Required Memo Sections

- Opportunity summary.
- Problem.
- Solution.
- Market.
- Timing.
- Thesis alignment.
- Evidence summary.
- Due diligence summary.
- Business model.
- Technical feasibility.
- Financial model.
- Expected ROI.
- Enterprise Value impact.
- Use of funds.
- Milestone plan.
- Risks.
- Dissent.
- Minority opinion.
- Strongest counter-argument.
- Dissent confidence.
- Founder override linkage where applicable.
- Legal/compliance review.
- Recommendation.
- Approval requirements.

Where relevant, the memo should include Organizational Memory context, Enterprise Knowledge Graph relationship context, Learning Engine outputs, and Reasoning Engine recommendations with source citations, assumptions, confidence, uncertainty, and dissent.

## Rule

Investment Memo is not a legal offering document.

It is an internal governed decision artifact unless future compliance explicitly permits investor-facing use.

## Governance Requirements

Investment Memo must preserve evidence, assumptions, forecasts, dissent, legal/compliance review status, and approval requirements.

Reasoning output included in an Investment Memo must remain classified as reasoning unless promoted through Evidence governance. The memo must not convert reasoning output into Evidence automatically.

## Dissent Preservation

Investment Memo must preserve material dissent from Debate Engine, Consensus Engine, Dynamic Review Council, Strategic Review Domain, Reasoning Engine outputs, and human reviewers where applicable.

Every governed Investment Memo must include minority opinion or explicitly state that no material minority opinion was identified.

Every governed Investment Memo must include the strongest counter-argument to the recommended action.

Dissent confidence must be recorded so Founder can distinguish weak concerns from high-confidence objections.

If Founder overrides dissent, the Founder Decision must link to the dissent record.

## Placeholder Status

This is architecture documentation only. It does not define legal offering documents, investor materials, schemas, services, or implementation.
