# ADR-093: Reasoning Input Freshness

Parent: `docs/architecture/reasoning-engine.md`

Status: Accepted

## Context

Reasoning quality depends on the freshness of Evidence, Knowledge Graph nodes, Memory records, and Learning records.

## Decision

Reasoning outputs must include input freshness status, stale node declarations, and superseded knowledge handling.

## Alternatives

- Trust graph data without freshness declaration.
- Use only Evidence freshness and ignore Knowledge Graph nodes.
- Leave freshness to reviewers.

## Rationale

Stale or superseded inputs can produce misleading recommendations if not visible.

## Risks

Some historical reasoning may require careful classification.

## Consequences

Reasoning Engine, Enterprise Knowledge Graph, and Evidence Freshness and Quality Model must expose freshness status.

## Enforcement

Reasoning outputs must not hide stale, expired, superseded, withdrawn, or unknown-freshness inputs behind aggregate confidence.
