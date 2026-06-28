# AI Gateway

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for AI Gateway architecture.

## Purpose

The AI Gateway is the only permitted path from the system to AI providers.

## Rules

- AI provider access must be gateway-controlled.
- Secrets must never be sent in prompts.
- Provider-specific behavior must remain behind the gateway abstraction.
- AI usage must be auditable where meaningful decisions or actions are affected.

