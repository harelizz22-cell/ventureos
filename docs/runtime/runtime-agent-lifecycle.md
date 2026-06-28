# Runtime Agent Lifecycle

Parent: `docs/runtime/README.md`

Source Of Truth: This file is the source of truth for runtime agent lifecycle behavior.

## Purpose

Define how approved VentureOS runtime agents move through operating states after activation.

## Scope

This document covers runtime lifecycle behavior for approved agents. Agent creation and activation governance belongs to `docs/architecture/agent-evolution.md`.

## Non-goals

- No agent implementation code.
- No runtime framework selection.
- No new agent roles.
- No activation approval bypass.

## Architectural Rules

- Agents may not activate themselves.
- Agents may not modify their own contracts.
- Agents may not approve their own work.
- Runtime state changes must be auditable.
- Suspended agents must not execute governed actions.

## Open Questions

- What runtime states are required beyond active, suspended, failed, and retired?
- What events must be emitted for each lifecycle transition?
- What founder-facing controls are required for lifecycle intervention?

