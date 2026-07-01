# System Health Model

Parent: `docs/architecture/observability-architecture.md`

Source Of Truth: This file is the source of truth for System Health Model architecture.

## Purpose

System Health Model defines how VentureOS reports health across business, runtime, governance, treasury, knowledge, AI, and infrastructure layers.

## Health Score Contract

Every health score must include:

- Status.
- Confidence.
- Risk.
- Trend.
- Recommended action.

Recommended actions are advisory unless routed through governed execution and Policy Engine approval.

## Status Values

Allowed status values:

- Healthy.
- Degraded.
- At Risk.
- Blocked.
- Unknown.

Unknown must be treated conservatively for governed or capital-sensitive action.

## Organization Health

Measures Organization-level operating health across governance, capital, portfolios, incidents, policy, evidence, and Enterprise Value trend.

## Portfolio Health

Measures portfolio health across Ventures, diversification, concentration, capital exposure, expected return, incidents, and Enterprise Value trend.

## Venture Health

Measures Venture health across execution, validation, revenue, cost, risk, evidence, incidents, and operational readiness.

## Runtime Health

Measures Runtime Kernel, Execution API, scheduler, event flow, recovery, resource coordination, and safe mode status.

## Execution Health

Measures running, failed, delayed, retried, blocked, recovered, and escalated executions.

## Workflow Health

Measures workflow reliability, queue delay, step failure, dependency availability, policy blocks, and outcome completion.

## Agent Health

Measures agent permission scope, task reliability, output quality, policy denials, autonomy level, and governance compliance.

Agents remain implementation options and must not approve their own health-based promotion.

## Capability Health

Measures capability availability, reliability, ownership, policy compliance, evidence linkage, cost, and business outcome contribution.

## Knowledge Health

Measures knowledge freshness, source quality, classification, provenance, graph consistency, memory durability, learning status, and reasoning safety.

## Treasury Health

Measures capital lifecycle integrity, available capital, reserved capital, committed capital, release blocks, spend verification, recovered capital, treasury risk, emergency lock, and security alerts.

Treasury Health does not authorize money movement.

## Infrastructure Health

Measures infrastructure availability, latency, capacity, dependency state, failure rate, incident load, recovery readiness, and deployment safety for future implementation.

## Health Score Requirements

Each score must identify:

- Scope.
- Timestamp.
- Source signals.
- Confidence.
- Staleness.
- Recommended action.
- Policy or approval requirement when action is proposed.

## Placeholder Status

This is architecture documentation only. It does not define scoring formulas, monitoring systems, dashboards, schemas, services, dependencies, or implementation.
