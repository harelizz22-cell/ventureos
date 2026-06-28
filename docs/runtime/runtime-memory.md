# Runtime Memory

Parent: `docs/runtime/README.md`

Source Of Truth: This file is the source of truth for runtime memory behavior.

## Purpose

Define how VentureOS runtime behavior should treat memory, context, retained facts, and historical operating records.

## Scope

This document covers runtime memory principles. It does not define database schema, vector storage, model memory implementation, or vendor-specific systems.

## Non-goals

- No database schema.
- No storage vendor decision.
- No embedding strategy.
- No implementation code.

## Architectural Rules

- Runtime memory must not contain secrets.
- Memory used for meaningful decisions must link to evidence or decision records.
- Memory must distinguish durable facts from stale context and assumptions.
- Founder-owned data must remain founder-controlled.
- Audit-relevant memory must be reviewable.

## Open Questions

- Which runtime memories are durable versus session-scoped?
- What retention rules apply to research, decisions, and operating logs?
- What review process is required before memory affects autonomous action?

