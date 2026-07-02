# AI Model Registry

Parent: `docs/architecture/ai-gateway.md`

Source Of Truth: This file is the source of truth for AI Model Registry architecture.

## Purpose

AI Model Registry maintains governance over every AI model used by VentureOS.

The registry ensures AI Gateway invokes only approved models, model selection is governed, cost visibility is preserved, and model use remains auditable.

## Registry Fields

Every model record must define:

- Approved models.
- Prohibited models.
- Supported capabilities.
- Preferred workload classes.
- Cost profile.
- Latency profile.
- Quality profile.
- Context limits.
- Security classification.
- Reasoning suitability.
- Search suitability.
- Coding suitability.
- Document analysis suitability.
- Benchmark history.
- Approval status.
- Deprecation lifecycle.

## Approved Models

Approved models are models allowed for specific scopes, workload classes, capabilities, data classifications, and policy contexts.

Approval must include:

- Approving authority.
- Allowed use cases.
- Disallowed use cases.
- Cost profile.
- Security classification.
- Review date.
- Deprecation plan where applicable.

## Prohibited Models

Prohibited models must not be invoked by AI Gateway.

Reasons may include:

- Security risk.
- Data handling risk.
- Cost risk.
- Quality risk.
- Compliance risk.
- Deprecated status.
- Unapproved provider.

## Supported Capabilities

Model records must identify which capabilities a model may support, including reasoning, search, coding, document analysis, summarization, classification, extraction, validation, or other approved use cases.

## Preferred Workload Classes

Model records must identify preferred workload classes:

- Discovery / Research.
- Strategic Review.
- Runtime Execution.
- Treasury / Capital.
- Compliance / Legal.
- Founder Command.

Preferred workload class does not override Policy Engine, Cost Governance, AI Token Governance, security classification, or Founder approval thresholds.

## Cost Profile

Cost profile records expected relative cost, token sensitivity, budget implications, and Cost Governance considerations.

Treasury must receive model cost information where it affects financial visibility or budget state.

## Latency Profile

Latency profile records expected response speed and suitability for interactive, background, batch, research, or operational use.

## Quality Profile

Quality profile records expected quality for approved tasks and known limitations.

## Context Limits

Context limits define the model context capacity and safe operating boundaries.

## Security Classification

Security classification defines which data classifications and scopes the model may process.

Models may be restricted by Organization, Portfolio, Venture, data sensitivity, regulated domain, or compliance requirements.

## Suitability Dimensions

Reasoning suitability identifies whether a model may support reasoning outputs.

Search suitability identifies whether a model may support search, retrieval, ranking, or query expansion.

Coding suitability identifies whether a model may support code generation or code review after implementation approval.

Document analysis suitability identifies whether a model may support document parsing, extraction, summarization, or review.

## Benchmark History

Benchmark history records evaluation results, observed quality, cost, latency, failure modes, regressions, and review outcomes.

Benchmarks are review signals. They do not automatically approve a model.

## Approval Status

Allowed approval statuses:

- Proposed.
- Approved.
- Restricted.
- Deprecated.
- Prohibited.

## Deprecation Lifecycle

Deprecation lifecycle defines how models are phased out.

Deprecation records must include:

- Reason.
- Effective date.
- Replacement recommendation.
- Affected capabilities.
- Affected workload classes.
- Required migration review.

## Rules

- AI Gateway may invoke only approved models.
- Policy Engine governs model selection.
- Treasury receives model cost information.
- Observability tracks model performance.
- Reasoning Engine must record which model produced every recommendation.
- Prohibited, deprecated, or unapproved models must fail closed.
- Model selection must preserve Organization, Portfolio, Venture, actor, data classification, policy, and audit boundaries.

## Placeholder Status

This is architecture documentation only. It does not define model providers, API calls, credentials, benchmark tools, routing code, schemas, integrations, dependencies, or implementation.
