# ADR-041: Runtime Kernel

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Runtime Kernel decision.

## Status

Accepted

## Context

Phase 2 Workstream 01 decomposes overloaded runtime execution concerns into a Runtime Kernel foundation. VentureOS needs a kernel that runs the system without making business decisions.

## Decision

VentureOS adopts Runtime Kernel as the execution foundation of the system.

Runtime Kernel services are Execution Coordinator, Execution Scheduler, Approval Coordinator, Event Coordinator, Recovery Manager, Execution State Tracker, and Resource Coordinator.

## Alternatives considered

- Keep all runtime behavior inside Execution Orchestrator.
- Let Agents coordinate execution directly.
- Merge business review and execution runtime into one component.

## Rationale

Separating runtime coordination from business judgment preserves governance, auditability, capability-first architecture, and Founder control.

## Risks

- Kernel services may become implementation-heavy before architecture is approved.
- Runtime Kernel may be misunderstood as business decision authority.
- Service boundaries may drift without source-of-truth documentation.

## Consequences

- Execution Orchestrator is decomposed under Runtime Kernel.
- Runtime Kernel runs the system but does not make business decisions.
- Business decisions remain with Founder or approved governance policy.

## Enforcement

Runtime Kernel must not decide whether a business idea is good, whether capital should be allocated, whether an investment should be approved, or what strategy should be created.
