# Cost Governance

Parent: `docs/governance/governance-rules.md`

Source Of Truth: This file is the source of truth for cost governance principles.

## Purpose

Cost is an architectural concern, not merely an operational concern.

Cost Governance defines how VentureOS treats resource consumption, budget awareness, and future cost-based approval inputs.

AI Token Governance is defined in `docs/architecture/ai-token-governance.md`.

## Scope

Cost Governance applies to:

- AI provider costs.
- Execution costs.
- Infrastructure costs.
- Workflow costs.
- Retry costs.
- Token budgets.
- Developer time.
- Founder time.
- Third-party costs.
- Future funding process costs.
- Future investor marketplace costs.
- Future compliance review costs.
- Future budget enforcement.
- Future optimization engine.

## Principles

- Every execution consumes Resources.
- Cost must be visible before governed execution where meaningful.
- Cost risk may require founder approval.
- Retry behavior must account for cost.
- Token budgets are governance inputs, not prompt suggestions.
- Tokens are financial resources.
- Token usage must be attributed to Organization, Portfolio, Venture, Capability, Agent, and Execution.
- Token limits must allow operational breathing room but prevent uncontrolled waste.
- Founder may configure token approval thresholds.
- No autonomous system may increase token budget without governance approval.
- Cost optimization must not bypass evidence, decision, approval, audit, or recovery rules.
- Cost optimization must not bypass legal/compliance review for future investor marketplace or funding activity.
- The cheapest execution is not always correct.
- The most expensive execution is not always justified.

## Future Budget Enforcement

Future Policy Engine rules may use Cost Governance as an approval input.

Examples of future policy inputs include budget remaining, estimated execution cost, retry cost exposure, AI token usage, infrastructure spend, and portfolio-level cost limits.

AI Gateway must enforce bounded token usage where policy requires it and report token usage records to Cost Governance, Treasury, Observability, and Audit where applicable.

Token budgets must support soft limits, hard limits, emergency override, Founder approval thresholds, forecasting, monitoring, waste detection, runaway execution detection, repeated prompt detection, low-value execution detection, model selection by cost/value, efficiency scoring, audit, and escalation.

## Future Optimization Engine

A future optimization engine may recommend lower-cost execution paths. It may not override governance or founder approval.

## Non-Goals

- No billing integration.
- No provider pricing model.
- No budget schema.
- No implementation code.
- No secrets or account values.
- No investor fund custody.
- No securities transaction processing.
