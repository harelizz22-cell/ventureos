# ADR-083: AI Token Governance

Status: Accepted

Date: 2026-07-02

## Context

Phase 2 readiness review requires explicit control over AI token usage before implementation planning.

AI tokens are a financial resource. Without clear limits, attribution, monitoring, and escalation, AI execution may create uncontrolled waste, runaway execution, unclear cost ownership, and governance bypass risk.

## Decision

Adopt AI Token Governance as the architecture source of truth for token budgets, scoped limits, soft limits, hard limits, emergency override, Founder approval thresholds, cost attribution, forecasting, monitoring, waste detection, runaway execution detection, repeated prompt detection, low-value execution detection, model selection by cost/value, token efficiency scoring, audit, and escalation.

Token usage must be attributed to Organization, Portfolio, Venture, Capability, Agent, and Execution.

AI Gateway must not allow unbounded token consumption.

Discovery / Research workloads receive a flexible budget exception because they are expected to be high-token consumers that collect intelligence for the broader VentureOS decision system.

Flexible Discovery / Research budgets are still governed. They require attribution, monitoring, soft budgets, anomaly detection, waste detection, Founder-configurable limits, escalation thresholds, research quality justification, cost-per-insight tracking, cost-per-evidence tracking, and stop conditions for runaway loops.

No workload has unlimited token spending.

## Alternatives

- Defer token governance to implementation.
- Let AI Gateway only report token usage after execution.
- Treat token budgets as informal prompt guidance.
- Apply only global token limits without Organization, Portfolio, Venture, Capability, Agent, and Execution attribution.
- Give Discovery / Research unlimited token usage because research is exploratory.

## Rationale

Token usage is cost-bearing resource consumption and must be governed before high-cost AI execution can be safely planned.

Soft limits allow operational breathing room. Hard limits prevent uncontrolled waste. Founder approval thresholds preserve human authority.

Discovery / Research needs more breathing room than strict execution classes, but unbounded research would violate capital discipline and cost governance.

## Risks

- Overly strict limits may block useful work.
- Overly loose limits may allow waste.
- Forecasting may be inaccurate.
- Model selection may optimize cost at the expense of quality if governance is poorly designed.
- Token usage audit may expose sensitive prompt details if not scoped carefully.
- Discovery / Research flexible budgets may be abused unless cost-per-insight, cost-per-evidence, anomaly detection, and stop conditions are enforced.

## Consequences

- AI Gateway must enforce bounded token consumption.
- Policy Engine evaluates high-cost AI execution against token budget rules.
- Treasury and Cost Governance receive token usage records.
- Founder may configure approval thresholds.
- Discovery / Research may use high-flexibility, high-monitoring token budgets.
- Cost per insight and cost per evidence item become review signals where meaningful.
- No autonomous system may increase token budget without governance approval.

## Enforcement

Future implementation must route token-consuming AI execution through AI Gateway, Resource Coordinator, Cost Governance, Policy Engine, Observability, and Audit requirements.

Hard limit uncertainty, unavailable budget state, missing attribution, or missing token usage records must fail closed for governed high-cost AI execution.
