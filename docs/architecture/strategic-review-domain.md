# Strategic Review Domain

Parent: `docs/architecture/domain-model.md`

Source Of Truth: This file is the source of truth for Strategic Review Domain architecture.

## Purpose

Define the domain responsible for structured business review before VentureOS recommends building, investing, funding, scaling, pausing, or exiting.

The Strategic Review Domain learns from professional venture capital operating patterns such as investment thesis, deal sourcing, due diligence, investment memo, investment committee, stage gates, portfolio construction, follow-on reserves, risk review, legal/compliance review, and post-investment monitoring.

These patterns are architectural inspiration only. VentureOS does not copy any VC firm.

## Rule

Strategic Review Domain makes recommendations.

It does not execute decisions.

Founder or approved governance policy makes final decisions.

## Owns

- Dynamic Review Council.
- Debate Engine.
- Consensus Engine.
- Recommendation Generator.
- Confidence Engine.
- Dissent Recorder.
- Investment Memo Generator.
- Review Evidence Pack.

## Responsibilities

- Assemble structured opportunity reviews.
- Coordinate multi-perspective review.
- Capture evidence, assumptions, risks, dissent, and confidence.
- Produce governed recommendations.
- Produce internal Investment Memos for major capital decisions.
- Use approved knowledge, Organizational Memory, Enterprise Knowledge Graph context, Learning Engine outputs, and Reasoning Engine recommendations where policy permits.

## Non-Responsibilities

- Final Founder decision.
- Investment execution.
- Capital movement.
- Runtime execution coordination.
- Legal offering documents.
- Treating reasoning output as Evidence without Evidence Promotion governance.

## Knowledge And Reasoning Inputs

Strategic Review Domain may consume Enterprise Knowledge Graph relationships, Organizational Memory records, Learning Engine outputs, and Reasoning Engine recommendations.

These inputs strengthen long-term organizational intelligence and review quality, but they do not replace Evidence, Thesis review, Hypothesis approval, Debate, dissent, Founder approval, or approved governance policy.

## Placeholder Status

This is architecture documentation only. It does not define agents, services, prompts, schemas, integrations, legal documents, or implementation.
