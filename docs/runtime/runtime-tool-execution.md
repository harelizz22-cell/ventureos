# Runtime Tool Execution

Parent: `docs/runtime/README.md`

Source Of Truth: This file is the source of truth for runtime tool execution behavior.

## Purpose

Define how VentureOS runtime behavior handles tool execution requests.

## Scope

This document covers runtime behavior for tool execution. Tool Gateway architecture belongs to `docs/architecture/tool-gateway.md`, and tool contract format belongs to `docs/contracts/tool-contract-template.md`.

## Non-goals

- No tool implementation.
- No external integration.
- No credentials.
- No tool vendor decision.

## Architectural Rules

- Agents must not access external tools directly.
- Tool execution must route through Tool Gateway.
- Tool execution must pass policy evaluation.
- Tool execution must be auditable.
- Tool execution must not expose secrets to agents, prompts, logs, commits, or documentation.

## Open Questions

- What tool execution request states are required?
- What approval thresholds apply to tool execution?
- Which tool execution events are required for auditability?

