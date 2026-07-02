# AI Gateway

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for AI Gateway architecture.

## Purpose

The AI Gateway is the only permitted path from the system to AI providers.

AI output classification is defined in `docs/architecture/ai-output-classification.md`.

AI token usage governance is defined in `docs/architecture/ai-token-governance.md`.

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

## Token Governance Decision

AI Gateway must enforce bounded token usage before and during governed AI execution where policy requires it. It must also report token usage after execution to Cost Governance, Treasury, Observability, and Audit where applicable.

Token budget rules are no longer an open decision.
