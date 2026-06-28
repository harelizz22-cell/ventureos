# Runtime Autonomy Levels

Parent: `docs/runtime/README.md`

Source Of Truth: This file is the source of truth for runtime autonomy level behavior.

## Purpose

Define how VentureOS runtime behavior is constrained by autonomy level.

## Scope

This document covers operating behavior for autonomy levels. It does not authorize higher autonomy levels or implementation.

## Non-goals

- No autonomous execution implementation.
- No approval threshold values.
- No production policy engine code.
- No permission escalation.

## Architectural Rules

- Current configuration starts at Autonomy Level 1: Assisted Mode.
- Higher autonomy levels require founder approval.
- Autonomy does not override governance.
- Agents cannot self-approve autonomy expansion.
- Runtime actions must follow policy, evidence, approval, audit, and recovery rules.

## Open Questions

- What exact runtime permissions belong to each autonomy level?
- What evidence is required to move from Level 1 to Level 2?
- What rollback controls are required for semi-autonomous and autonomous operation?

