# Operations Dashboard

Parent: `docs/architecture/observability-architecture.md`

Source Of Truth: This file is the source of truth for Operations Dashboard architecture.

## Purpose

Operations Dashboard defines the founder-visible and operator-visible control surface for system operations, health, incidents, execution state, policy issues, treasury alerts, and operational readiness.

This dashboard is visibility and decision support. It does not approve execution, move money, override governance, or bypass Policy Engine.

## Founder Visibility

Founder should always see:

- System Health.
- Portfolio Health.
- Execution Queue.
- Policy Violations.
- Treasury Alerts.
- Open Incidents.
- Running Executions.
- Failed Executions.
- Capital Exposure.
- Enterprise Value Trend.
- AI Token Usage.
- Token Budget Alerts.

## System Health

System Health summarizes Organization, Portfolio, Venture, Runtime, Execution, Workflow, Agent, Capability, Knowledge, Treasury, and Infrastructure health.

## Portfolio Health

Portfolio Health summarizes Venture health, diversification, concentration, capital exposure, incidents, execution state, and Enterprise Value trend.

## Execution Queue

Execution Queue shows queued, running, blocked, waiting for approval, retrying, failed, recovered, and cancelled executions.

## Policy Violations

Policy Violations show denials, fail-closed outcomes, policy evaluator disagreement, governance lag, missing approval, and blocked autonomy escalation.

## Treasury Alerts

Treasury Alerts show lifecycle inconsistency, reservation conflict, emergency lock, high-risk release, spend verification issue, capital exposure warning, and treasury security alerts.

Treasury Alerts do not authorize money movement.

## Open Incidents

Open Incidents show severity, priority, owner, status, impact, escalation path, recovery state, and audit linkage.

## Running Executions

Running Executions show scope, owner, start time, policy result, current step, trace, timeout risk, and recovery readiness.

## Failed Executions

Failed Executions show failure taxonomy, retry eligibility, idempotency state, recovery path, incident linkage, and required approval.

## Capital Exposure

Capital Exposure shows available, reserved, committed, approved, released, spent, verified, recovered, cancelled, and closed capital where applicable.

## AI Token Usage

AI Token Usage shows token consumption by Organization, Portfolio, Venture, Capability, Agent, and Execution.

AI Token Usage must show workload class, budget state, soft-limit status, hard-limit status, approval thresholds, cost attribution, forecast variance, and waste signals where applicable.

Discovery / Research views must show flexible-budget status, research quality justification, cost per insight, cost per evidence item, anomaly signals, escalation thresholds, and runaway loop stop conditions.

## Token Budget Alerts

Token Budget Alerts show soft limit warnings, hard limit blocks, runaway execution detection, repeated prompt detection, low-value execution detection, emergency override use, and missing token usage records.

Token Budget Alerts do not authorize additional token budget.

No dashboard view may grant unlimited token usage.

## Enterprise Value Trend

Enterprise Value Trend shows business outcome direction, risk, confidence, and supporting signals without guaranteeing returns.

## Governance Rules

- Dashboard actions must route through Execution API and Policy Engine.
- Dashboard views must respect Organization, Portfolio, Venture, actor, role, and classification boundaries.
- AI summaries are not Evidence until promoted.
- Audit records must be preserved for approvals, denials, incident actions, and capital-sensitive decisions.

## Placeholder Status

This is architecture documentation only. It does not define UI, charts, APIs, schemas, services, telemetry systems, dependencies, or implementation.
