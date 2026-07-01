# ADR-078: System Health Model

Status: Accepted

Date: 2026-07-01

## Context

VentureOS needs consistent health reporting across business, runtime, governance, treasury, AI, knowledge, and infrastructure concerns.

## Decision

Adopt System Health Model with health at Organization, Portfolio, Venture, Runtime, Execution, Workflow, Agent, Capability, Knowledge, Treasury, and Infrastructure levels.

Every health score must include status, confidence, risk, trend, and recommended action.

## Rationale

Health must be comparable and explainable across the whole system, not limited to infrastructure uptime.

## Consequences

- Health scores become operational signals.
- Unknown health is treated conservatively for governed or capital-sensitive action.
- Recommended actions remain advisory unless routed through governed execution.

## Enforcement

Future health reporting must identify scope, timestamp, source signals, confidence, staleness, recommended action, and governance requirements.
