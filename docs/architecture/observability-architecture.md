# Observability Architecture

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Observability Architecture.

## Purpose

Observability Architecture defines how VentureOS is monitored, measured, diagnosed, audited, and operated.

Observability is an architecture requirement, not an implementation choice. It does not authorize production code, integrations, telemetry vendors, dashboards, or infrastructure.

## Three Pillars

### Metrics

Metrics are measurable signals about system behavior, business operation, governance health, reliability, and operational risk.

Metrics must support:

- System health.
- Execution reliability.
- Policy enforcement.
- Treasury alerts.
- AI behavior review.
- Enterprise Value and portfolio visibility.

Metrics do not become Evidence automatically. Metrics may support Evidence only through governed promotion and review.

### Logs

Logs are structured operational records that explain what happened.

Logs must include:

- Actor or component.
- Organization, Portfolio, Venture, Capability, Workflow, and Execution scope where applicable.
- Event or action.
- Outcome.
- Error or denial reason.
- Correlation ID.
- Timestamp.
- Policy version or snapshot where applicable.

Logs are operational records. Audit Ledger remains the authoritative append-only audit concern.

### Distributed Tracing

Distributed tracing connects related steps across Runtime Kernel, Execution API, Policy Engine, Tool Gateway, AI Gateway, Treasury, Knowledge, and other future services.

Traces must show:

- Request entry point.
- Capability invocation.
- Policy evaluation.
- Approval wait.
- Tool or AI interaction.
- Treasury-sensitive operation.
- Recovery or incident path.
- Execution completion or failure.

## Metrics

Metrics must include runtime, execution, workflow, policy, treasury, AI, knowledge, infrastructure, and portfolio health signals where applicable.

Metric categories:

- Availability.
- Latency.
- Error rate.
- Queue depth.
- Retry rate.
- Recovery rate.
- Policy denial rate.
- Approval wait time.
- Treasury alert count.
- AI output classification distribution.
- Token usage by Organization, Portfolio, Venture, Capability, Agent, and Execution.
- Token soft-limit and hard-limit events.
- Token waste, repeated prompt, low-value execution, and runaway execution signals.
- Discovery / Research cost per insight, cost per evidence item, anomaly signals, research quality justification, and runaway loop stop conditions.
- Evidence freshness.
- Incident frequency.

## Logs

Logs must support diagnosis without exposing secrets, credentials, regulated data, private tenant data, or unauthorized Venture data.

Logs must preserve Organization, Portfolio, Venture, actor, role, classification, and Policy Engine boundaries.

## Traces

Traces must preserve execution causality.

Trace records should connect Execution API request, Policy Engine outcome, Runtime Kernel state, Capability, Workflow, Event, Evidence, Decision, Audit, recovery, and incident references.

## Health Checks

Health checks must determine whether required components are available and safe to use.

Required health checks include:

- Runtime Kernel health.
- Execution API health.
- Policy Engine health.
- Evidence, Decision, and Audit Ledger availability.
- Event pipeline health.
- Knowledge and memory health.
- Treasury lifecycle health.
- AI Gateway safety status.
- Tool Gateway safety status.

If Policy Engine health fails, governed execution must fail closed.

## Dependency Monitoring

Dependency monitoring tracks required internal and future external dependencies.

Dependency health must include status, latency, errors, policy availability, data freshness, and degradation impact.

## Runtime Diagnostics

Runtime diagnostics explain current runtime state, queue pressure, event flow, resource contention, policy availability, recovery state, and safe mode status.

## Execution Diagnostics

Execution diagnostics explain execution state transitions, retries, idempotency, timeouts, failures, recovery attempts, compensation, rollback, forward recovery, and incident linkage.

## Policy Diagnostics

Policy diagnostics explain policy version, policy snapshot, evaluator status, denial reason, approval requirements, governance lag, conflict handling, and fail-closed behavior.

## Treasury Diagnostics

Treasury diagnostics explain capital lifecycle state, reservations, commitments, releases, spend verification, recovery, cancelled capital, emergency freeze, treasury risk, and treasury security alerts.

Treasury diagnostics must never authorize money movement.

## AI Diagnostics

AI diagnostics explain AI request scope, model or provider class, prompt classification, output classification, confidence, uncertainty, source citations, Evidence Promotion status, and policy constraints.

AI diagnostics must preserve the rule that AI output is not Evidence until promoted.

AI diagnostics must include token usage forecasting, token usage monitoring, cost attribution, model selection by cost/value, token efficiency scoring, token limit state, and token escalation state where applicable.

Observability must surface when AI Gateway cannot provide bounded token usage, attribution, or usage records.

Observability must distinguish workload classes so Discovery / Research high-token usage is monitored as expected exploration rather than automatically treated as waste.

## Audit Requirements

Observability must link operational signals to Audit where meaningful without replacing Audit Ledger.

Operational visibility must never rewrite historical Evidence, Decision, Event, or Audit records.

## Placeholder Status

This is architecture documentation only. It does not define telemetry tooling, logging libraries, tracing vendors, schemas, agents, infrastructure, integrations, secrets, or implementation.
