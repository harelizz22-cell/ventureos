# ADR-045: Strategic Review Domain

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Strategic Review Domain decision.

## Status

Accepted

## Context

VentureOS needs structured business review before recommending build, investment, funding, scaling, pause, or exit actions. Professional venture capital operating patterns provide useful architectural inspiration without being copied.

## Decision

VentureOS adopts Strategic Review Domain as the domain responsible for structured opportunity review.

Strategic Review Domain owns Dynamic Review Council, Debate Engine, Consensus Engine, Recommendation Generator, Confidence Engine, Dissent Recorder, Investment Memo Generator, and Review Evidence Pack.

## Alternatives considered

- Put strategic review inside Runtime Kernel.
- Let single agents produce recommendations without structured review.
- Treat venture capital operating patterns as implementation workflow instead of architecture inspiration.

## Rationale

Structured review improves decision quality, preserves dissent, strengthens evidence, and keeps runtime execution separate from business judgment.

## Risks

- Strategic Review Domain may be mistaken for final decision authority.
- Review processes may become too heavy for low-risk decisions.
- VC-inspired patterns may be copied too literally instead of adapted.

## Consequences

- Strategic Review Domain makes recommendations only.
- Founder or approved governance policy makes final decisions.
- Business review becomes a formal architecture concern.

## Enforcement

Strategic Review Domain must not execute decisions, approve investments, move money, or bypass Founder/governance authority.
