# AI Token Governance

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for AI Token Governance architecture.

## Purpose

AI Token Governance defines how VentureOS controls AI token usage, prevents waste, attributes cost, and allows necessary execution flexibility.

Tokens are financial resources.

AI Token Governance is a governance and cost-control architecture concern. It does not authorize production code, provider integrations, billing integrations, pricing schemas, secrets, or implementation.

## Core Rules

- Tokens are financial resources.
- Token usage must be attributed to Organization, Portfolio, Venture, Capability, Agent, and Execution.
- AI Gateway must not allow unbounded token consumption.
- Policy Engine must evaluate token budget rules before high-cost AI execution.
- Treasury and Cost Governance must receive token usage records.
- Token limits must allow operational breathing room but prevent uncontrolled waste.
- Founder may configure approval thresholds.
- No autonomous system may increase token budget without governance approval.

## Token Budgets

Token budgets define planned and allowable AI token consumption for governed scopes.

Budget dimensions:

- Expected token usage.
- Maximum token usage.
- Soft limit.
- Hard limit.
- Time window.
- Approval threshold.
- Scope.
- Owner.
- Policy requirement.

Token budgets are governance inputs, not prompt suggestions.

## Per-Organization Limits

Organization limits define the maximum token exposure for an Organization across all Portfolios, Ventures, Capabilities, Agents, and Executions.

Organization limits protect tenant-level financial discipline and must be visible to Cost Governance, Treasury, Policy Engine, and Founder-facing operations views.

## Per-Portfolio Limits

Portfolio limits define token usage boundaries across Ventures inside a Portfolio.

Portfolio limits must support fair allocation, capital exposure awareness, and portfolio-level cost review.

## Per-Venture Limits

Venture limits define token usage boundaries for a Venture.

Venture limits must support validation, build, operations, research, and recovery work without allowing unbounded experimentation.

## Per-Capability Limits

Capability limits define token usage boundaries for a specific Capability.

Capability limits must account for expected business value, Evidence requirements, output criticality, risk, and cost/value profile.

## Per-Agent Limits

Agent limits define token usage boundaries for an Agent or future AI participant.

Agent limits must prevent runaway planning, repeated prompt loops, excessive self-review, and unauthorized autonomy expansion.

Agents may not increase their own token budgets.

## Per-Execution Limits

Execution limits define the maximum token usage allowed for a single Execution attempt, retry, recovery path, or workflow step.

Executions must preserve token usage estimates, actual token usage, remaining budget, and escalation status.

## Soft Limits

Soft limits are warning thresholds that allow execution to continue while triggering visibility, monitoring, and possible approval requirements.

Soft limit behavior may include:

- Warning.
- Founder visibility.
- Cost Governance review.
- Model downgrade recommendation.
- Prompt compression recommendation.
- Execution checkpoint.
- Approval requirement for continued high-cost execution.

## Hard Limits

Hard limits are enforced stop conditions.

Hard limit behavior:

- Block new token-consuming work in the affected scope.
- Stop or pause execution at the next safe boundary.
- Require governed approval before continuation.
- Create audit and observability records.

Hard limits must fail closed when budget state cannot be verified.

## Emergency Override

Emergency override allows token usage beyond normal limits only for governed exceptional cases such as recovery, incident response, security response, or Founder-approved urgent work.

Emergency override requirements:

- Policy Engine evaluation.
- Founder approval or explicitly approved governance path.
- Scope.
- Reason.
- Maximum additional token allowance.
- Expiration.
- Audit record.

No autonomous system may grant itself emergency override.

## Founder Approval Thresholds

Founder may configure approval thresholds by Organization, Portfolio, Venture, Capability, Agent, Execution, time window, cost estimate, risk, model class, and purpose.

Thresholds may trigger:

- Continue.
- Require Founder approval.
- Require cost review.
- Require risk review.
- Deny.
- Fail closed.

## Cost Attribution

Token usage must be attributed to:

- Organization.
- Portfolio.
- Venture.
- Capability.
- Agent.
- Execution.

Where meaningful, token usage should also include Workflow, actor, model class, purpose, request category, policy version, and correlation ID.

## Token Usage Forecasting

Token usage forecasting estimates likely token consumption before execution.

Forecasting inputs may include:

- Prompt size.
- Context size.
- Expected output size.
- Model class.
- Retrieval volume.
- Tool use pattern.
- Retry risk.
- Recovery risk.
- Prior usage for similar Executions.

Forecasts must distinguish estimate, uncertainty, and approval relevance.

## Token Usage Monitoring

Token usage monitoring tracks estimated, reserved, actual, cumulative, anomalous, failed, retried, and wasted token usage.

Monitoring must feed Observability, Operations Dashboard, Cost Governance, Treasury, Policy Engine, and Audit where applicable.

## Waste Detection

Waste detection identifies token usage that does not produce proportional business, evidence, operational, recovery, or governance value.

Waste signals:

- Excessive retries.
- Repeated prompts.
- Low-value outputs.
- Unused generated content.
- Duplicative research.
- Unbounded reasoning loops.
- Overly expensive model selection.

Waste detection is a signal, not an automatic Decision.

## Runaway Execution Detection

Runaway execution detection identifies token-consuming execution that exceeds expected time, iterations, token growth, retry count, output churn, or policy bounds.

Runaway behavior must trigger pause, escalation, incident creation, or hard-limit enforcement where policy requires it.

## Repeated Prompt Detection

Repeated prompt detection identifies identical or substantially similar prompts that consume tokens without new Evidence, Decision, or operational value.

Repeated prompt findings may trigger deduplication, prompt revision, cache review, human review, or block.

## Low-Value Execution Detection

Low-value execution detection identifies executions whose token usage is high relative to expected Enterprise Value, evidence value, operational value, recovery value, or governance value.

Low-value detection may trigger model selection review, prompt compression, approval requirement, or denial.

## Model Selection By Cost And Value

Model selection must consider:

- Required quality.
- Required reasoning depth.
- Risk.
- Evidence need.
- Context size.
- Cost.
- Latency.
- Confidence requirement.
- Auditability.
- Expected value.

The cheapest model is not always correct. The most expensive model is not always justified.

High-cost model use may require Policy Engine evaluation and Founder approval where thresholds require it.

## Token Efficiency Scoring

Token efficiency scoring compares token usage against useful output, evidence quality, decision support, execution progress, recovery value, and Enterprise Value contribution.

Token efficiency is an operational and governance signal. It must not override Evidence, Policy Engine, Founder approval, or safety requirements.

## Token Usage Audit

Token usage audit records must include:

- Scope attribution.
- Estimated tokens.
- Actual tokens where available.
- Model class.
- Purpose.
- Policy result.
- Soft or hard limit status.
- Approval record where required.
- Cost Governance record.
- Treasury record.
- Execution correlation ID.
- Timestamp.

Token usage audit must not expose secrets, private prompts, or unauthorized data.

## Escalation Rules

Escalation is required when:

- Hard limit is reached.
- Soft limit is repeatedly exceeded.
- High-cost execution crosses Founder approval threshold.
- Runaway execution is detected.
- Repeated prompt waste is detected.
- Low-value execution persists.
- Budget state cannot be verified.
- AI Gateway cannot produce token usage records.
- Treasury or Cost Governance cannot receive required usage records.

Escalation may route to Founder, Cost Governance, Policy Engine, Treasury, Incident Management, or Operations Dashboard depending on severity and scope.

## Placeholder Status

This is architecture documentation only. It does not define token accounting schemas, provider APIs, pricing data, billing integrations, telemetry tooling, secrets, services, dependencies, or implementation.
