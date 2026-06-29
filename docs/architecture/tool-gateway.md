# Tool Gateway

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Tool Gateway architecture.

## Purpose

The Tool Gateway is the only permitted path from agents to external tools.

## Rules

- Agents request tool actions; they do not hold credentials.
- Tool actions must pass policy evaluation.
- Tool actions must be auditable.
- Tool contracts belong in `docs/contracts/`.
- External tool calls must use idempotency keys where possible.
- For external calls with ambiguous outcome, automatic retry is forbidden unless the tool contract proves idempotency.
- Ambiguous external side effects must create an Incident or require review.
