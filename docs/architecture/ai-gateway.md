# AI Gateway

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for AI Gateway architecture.

## Purpose

The AI Gateway is the only permitted path from the system to AI providers.

AI output classification is defined in `docs/architecture/ai-output-classification.md`.

AI token usage governance is defined in `docs/architecture/ai-token-governance.md`.

AI Model Registry is defined in `docs/architecture/ai-model-registry.md`.

## Rules

- AI provider access must be gateway-controlled.
- Secrets must never be sent in prompts.
- Provider-specific behavior must remain behind the gateway abstraction.
- AI usage must be auditable where meaningful decisions or actions are affected.
- AI output is never Evidence by default.
- AI output must follow Draft -> Recommendation -> Candidate Evidence -> Verified Evidence.
- AI output must be traceable to model, prompt, context, and source inputs where possible.
- AI hallucination risk must be mitigated through source citation, confidence, uncertainty, limitations, and promotion governance.
- AI Gateway must not allow unbounded token consumption.
- Token usage must be attributed to Organization, Portfolio, Venture, Capability, Agent, and Execution.
- AI Gateway must enforce token budget checks, soft limits, hard limits, emergency override rules, and Founder approval thresholds where policy requires them.
- AI Gateway must produce token usage records for Treasury and Cost Governance.
- AI Gateway must support token usage forecasting, token usage monitoring, waste detection, runaway execution detection, repeated prompt detection, low-value execution detection, model selection by cost/value, token efficiency scoring, token usage audit, and escalation.
- AI Gateway must recognize workload classes: Discovery / Research, Strategic Review, Runtime Execution, Treasury / Capital, Compliance / Legal, and Founder Command.
- Discovery / Research workloads may receive high-flexibility token budgets, but AI Gateway must still enforce attribution, monitoring, soft budgets, anomaly detection, waste detection, Founder-configurable limits, escalation thresholds, research quality justification, cost-per-insight tracking, cost-per-evidence tracking, and stop conditions for runaway loops.
- No workload may have unlimited token usage.
- AI Gateway may invoke only approved models from AI Model Registry.
- AI Gateway must fail closed when model approval status, security classification, policy suitability, or cost profile cannot be verified.
- AI Gateway must preserve model identity, workload class, cost profile, and policy context in audit records where meaningful.

## Token Governance Decision

AI Gateway must enforce bounded token usage before and during governed AI execution where policy requires it. It must also report token usage after execution to Cost Governance, Treasury, Observability, and Audit where applicable.

Token budget rules are no longer an open decision.

Discovery / Research flexibility is an approved budget class, not an exemption from governance.

## Token Reservation Enforcement

AI Gateway must verify required token reservation before token-consuming execution starts.

AI Gateway must enforce reservation amount, expiry, release condition, workload class, inheritance rules, hard limits, approved overrides, and attribution during execution.

If reservation state is missing, expired, over-consumed, or inconsistent, AI Gateway must pause, stop, escalate, or fail closed according to Policy Engine outcome.

AI Gateway must report reservation consumption, unused release, expiry, and over-consumption events to Treasury, Cost Governance, Observability, and Audit where applicable.

## Model Governance Decision

Model selection is governed by AI Model Registry and Policy Engine.

Provider-specific availability does not mean model approval.
