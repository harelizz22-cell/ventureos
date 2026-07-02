# ADR-084: Financial Feedback Loop

Status: Accepted

Date: 2026-07-02

## Context

Phase 2 internal readiness review identified a final architecture gap: capital allocation outcomes must systematically feed organizational learning.

VentureOS already has Capital Allocation, Learning Engine, Enterprise Knowledge Graph, and Enterprise Value architecture. The missing hardening item is the explicit feedback loop from expected return to actual outcome and reusable learning.

## Decision

Adopt Financial Feedback Loop architecture.

Every completed capital allocation must connect Capital Allocation, Execution, Business Outcome, Expected ROI, Actual ROI, Variance Analysis, Lessons Learned, Learning Engine, Enterprise Knowledge Graph, and Future Investment Decisions.

## Rationale

Capital discipline improves only when outcomes become evidence-backed learning. Without this loop, VentureOS may repeat bad capital allocation patterns or fail to compound successful ones.

## Risks

- ROI may be hard to measure for early or strategic Ventures.
- Attribution may be incomplete.
- Learning may be overgeneralized from weak evidence.
- Teams may mistake learning recommendations for automatic policy changes.

## Consequences

- No completed Venture may exit the lifecycle without producing organizational learning.
- Learning remains evidence-backed and auditable.
- Learning may inform future investment decisions.
- Learning never automatically changes policy.

## Enforcement

Future implementation planning must preserve links between capital allocation records, execution records, business outcomes, ROI variance, Evidence, Decisions, Audit, Learning Engine records, and Enterprise Knowledge Graph relationships.
