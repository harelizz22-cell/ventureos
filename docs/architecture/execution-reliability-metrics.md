# Execution Reliability Metrics

Parent: `docs/architecture/execution-reliability.md`

Source Of Truth: This file is the source of truth for Execution Reliability Metrics architecture.

## Purpose

Define the metrics VentureOS uses to evaluate execution reliability, retry health, recovery quality, and incident trends.

## Metrics

### Success Rate

Percentage of governed executions that complete successfully within policy, scope, timeout, and audit requirements.

### Failure Rate

Percentage of governed executions that fail by failure category, Capability, Domain, Venture, Organization, policy snapshot, or dependency where meaningful.

### Retry Rate

Frequency and proportion of executions requiring retry.

Retry Rate must distinguish successful retries, exhausted retries, unsafe retries, and blocked retries.

### Recovery Success Rate

Percentage of recovery attempts that complete safely according to Recovery Governance.

### Mean Recovery Time

Average time from failure detection to safe recovery outcome, escalation, or declared unresolved state.

### Execution Latency

Time from accepted execution request to completed, failed, paused, deferred, or escalated state.

### Timeout Frequency

Frequency of execution, approval, dependency, recovery, and long-running execution timeouts.

### Dead Letter Volume

Number and rate of failed requests, Events, messages, or execution records sent to Dead Letter handling.

Dead Letter volume should be tracked by failure category, Domain, Capability, Venture, dependency, and policy snapshot where meaningful.

### Incident Frequency

Frequency of incidents created from execution failures, recovery failures, repeated retries, circuit breaker events, audit risks, compliance risks, or capital-sensitive failures.

## Metric Governance

Reliability metrics are observability signals.

They may become Evidence for Decisions only through governed Evidence Promotion.

## Rule

Execution reliability metrics must support operational review, Founder visibility, recovery improvement, and governance, but must not replace Evidence, Decisions, Audit, Policy, or human approval where required.

## Placeholder Status

This is architecture documentation only. It does not define dashboards, telemetry systems, metric stores, schemas, services, integrations, or implementation.
