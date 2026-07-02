# ADR-085: AI Model Registry

Status: Accepted

Date: 2026-07-02

## Context

Phase 2 internal readiness review identified a final architecture gap: VentureOS needs explicit governance over which AI models may be used, where they may be used, and how their cost, quality, security, and performance are tracked.

AI Gateway, AI Token Governance, Policy Engine, Treasury, Observability, and Reasoning Engine require a governed model source of truth.

## Decision

Adopt AI Model Registry architecture.

The registry governs approved models, prohibited models, supported capabilities, preferred workload classes, cost profile, latency profile, quality profile, context limits, security classification, suitability dimensions, benchmark history, approval status, and deprecation lifecycle.

## Rationale

Model choice affects cost, quality, security, reasoning reliability, data handling, and auditability. It must be governed rather than left to ad hoc prompts or implementation defaults.

## Risks

- Model registry records may become stale.
- Overly restrictive model approval may slow useful work.
- Benchmark history may be misread as permanent quality.
- Cost optimization may be over-prioritized against quality or safety.

## Consequences

- AI Gateway may invoke only approved models.
- Policy Engine governs model selection.
- Treasury receives model cost information.
- Observability tracks model performance.
- Reasoning Engine records which model produced every recommendation.

## Enforcement

Future implementation planning must fail closed when model approval status, security classification, policy suitability, or cost profile cannot be verified.
