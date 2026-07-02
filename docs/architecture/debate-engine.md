# Debate Engine

Parent: `docs/architecture/strategic-review-domain.md`

Source Of Truth: This file is the source of truth for Debate Engine architecture.

## Purpose

Define structured debate between review participants.

## Debate Output

Debate output must include:

- Arguments for.
- Arguments against.
- Evidence cited.
- Assumptions.
- Confidence per participant.
- Disagreement areas.
- Unresolved questions.
- Risk objections.
- Minority opinions.
- Strongest counter-argument.
- Dissent confidence.
- Founder override linkage where applicable.

## Rule

Disagreement must not be erased.

Material dissent must be recorded.

Minority opinion is required for governed Strategic Review unless no dissent exists, in which case the memo must state that no material dissent was identified.

The strongest counter-argument must be preserved even when consensus is strong.

## Governance Requirements

Debate outputs must preserve evidence references, participant identity, confidence, dissent, and unresolved questions for audit and Founder review.

Dissent confidence must identify how strongly the dissenting participant or review perspective holds the objection.

Founder override linkage must connect dissent to any later Founder Decision that approves, rejects, pauses, or overrides the dissent.

Debate may use Reasoning Engine outputs, Enterprise Knowledge Graph relationships, Organizational Memory records, and Learning Engine outputs as inputs. Any reasoning-derived claim must cite source knowledge, Evidence records, assumptions, confidence, uncertainty, and dissent where relevant.

Reasoning output does not become Evidence automatically.

## Placeholder Status

This is architecture documentation only. It does not define debate algorithms, prompts, agent behavior, or implementation.
