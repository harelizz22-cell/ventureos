# Cost Governance

Parent: `docs/governance/governance-rules.md`

Source Of Truth: This file is the source of truth for cost governance principles.

## Purpose

Cost is an architectural concern, not merely an operational concern.

Cost Governance defines how VentureOS treats resource consumption, budget awareness, and future cost-based approval inputs.

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
- Future budget enforcement.
- Future optimization engine.

## Principles

- Every execution consumes Resources.
- Cost must be visible before governed execution where meaningful.
- Cost risk may require founder approval.
- Retry behavior must account for cost.
- Token budgets are governance inputs, not prompt suggestions.
- Cost optimization must not bypass evidence, decision, approval, audit, or recovery rules.
- The cheapest execution is not always correct.
- The most expensive execution is not always justified.

## Future Budget Enforcement

Future Policy Engine rules may use Cost Governance as an approval input.

Examples of future policy inputs include budget remaining, estimated execution cost, retry cost exposure, AI token usage, infrastructure spend, and portfolio-level cost limits.

Open decision: Should AI Gateway enforce per-Venture token and cost budgets in real time, or report usage after execution for Policy Engine and Cost Governance response?

## Future Optimization Engine

A future optimization engine may recommend lower-cost execution paths. It may not override governance or founder approval.

## Non-Goals

- No billing integration.
- No provider pricing model.
- No budget schema.
- No implementation code.
- No secrets or account values.
