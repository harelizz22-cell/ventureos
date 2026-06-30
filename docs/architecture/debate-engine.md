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

## Rule

Disagreement must not be erased.

Material dissent must be recorded.

## Governance Requirements

Debate outputs must preserve evidence references, participant identity, confidence, dissent, and unresolved questions for audit and Founder review.

Debate may use Reasoning Engine outputs, Enterprise Knowledge Graph relationships, Organizational Memory records, and Learning Engine outputs as inputs. Any reasoning-derived claim must cite source knowledge, Evidence records, assumptions, confidence, uncertainty, and dissent where relevant.

Reasoning output does not become Evidence automatically.

## Placeholder Status

This is architecture documentation only. It does not define debate algorithms, prompts, agent behavior, or implementation.
