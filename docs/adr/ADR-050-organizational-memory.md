# ADR-050: Organizational Memory

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Organizational Memory decision.

## Status

Accepted

## Context

VentureOS needs durable organizational history across ventures, experiments, investments, overrides, incidents, exits, acquisitions, lessons, and playbooks. Knowledge must not remain trapped in Agents, individual Ventures, or temporary execution context.

## Decision

VentureOS adopts Organizational Memory as the durable historical memory layer for what happened and what the organization remembers.

Organizational Memory is separate from Learning Engine, Enterprise Knowledge Graph, and Reasoning Engine.

## Alternatives considered

- Keep history only inside Venture-specific records.
- Treat Agent memory as organizational memory.
- Merge memory, learning, graph, and reasoning into one component.

## Rationale

Durable, scoped, auditable, and reusable memory allows VentureOS to retain institutional context while preserving governance and source traceability.

## Risks

- Memory may become stale or disconnected from source records.
- Temporary execution context may be mistaken for durable memory.
- Memory may be overused as Evidence without promotion or source checks.

## Consequences

- Organizational history becomes an explicit architecture concern.
- Memory records must preserve scope, source, and audit links.
- Learning, graph, and reasoning remain separate responsibilities.

## Enforcement

Organizational Memory must be durable, scoped, auditable, reusable, and linked to governed source records where meaningful.
