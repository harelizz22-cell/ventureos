# Runtime Events

Parent: `docs/runtime/README.md`

Source Of Truth: This file is the source of truth for runtime event behavior.

## Purpose

Define how VentureOS runtime behavior produces and consumes meaningful events.

## Scope

This document covers runtime event behavior. Event architecture belongs to `docs/architecture/event-architecture.md`, and event contract format belongs to `docs/contracts/event-contract-template.md`.

## Non-goals

- No event bus implementation.
- No vendor decision.
- No code.
- No complete event catalog.

## Architectural Rules

- Meaningful runtime events must be auditable.
- Events must not contain secrets.
- Events that affect decisions, approvals, assets, or autonomy must link to relevant records.
- Event names and payloads must follow documented event contracts before implementation.

## Open Questions

- Which runtime events are required for Phase -1 architecture specification?
- What event retention policy is required?
- Which events must be founder-visible in the Founder Command Center?

