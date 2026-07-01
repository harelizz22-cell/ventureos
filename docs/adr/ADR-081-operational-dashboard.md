# ADR-081: Operational Dashboard

Status: Accepted

Date: 2026-07-01

## Context

Founder and operators need a single operational visibility layer for system health, portfolio health, executions, incidents, policy violations, treasury alerts, and Enterprise Value trend.

## Decision

Adopt Operations Dashboard architecture.

Founder should always see System Health, Portfolio Health, Execution Queue, Policy Violations, Treasury Alerts, Open Incidents, Running Executions, Failed Executions, Capital Exposure, and Enterprise Value Trend.

## Rationale

Founder control depends on timely visibility into operational risk and system state.

## Consequences

- Dashboard is visibility and decision support only.
- Dashboard actions route through Execution API and Policy Engine.
- Treasury alerts do not authorize money movement.
- AI summaries are not Evidence until promoted.

## Enforcement

Future dashboard implementation must preserve tenant, role, actor, policy, treasury, audit, and Evidence boundaries.
