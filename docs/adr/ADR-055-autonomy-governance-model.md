# ADR-055: Autonomy Governance Model

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Autonomy Governance Model decision.

## Status

Accepted

## Context

VentureOS starts in Assisted Mode and must remain autonomy-ready. Higher autonomy requires governance, evidence, audit, recovery, and Founder approval before runtime behavior expands.

## Decision

VentureOS adopts the Autonomy Governance Model for autonomy levels, allowed and blocked actions, promotion, demotion, safe mode, emergency mode, partial autonomy, and Policy Engine enforcement.

## Alternatives considered

- Treat autonomy as a global system switch.
- Let Agents request or approve autonomy expansion.
- Define autonomy levels without runtime enforcement.

## Rationale

Autonomy governance preserves Founder control, prevents self-approval, and supports incremental, auditable autonomy expansion.

## Risks

- Partial autonomy may be difficult to reason about without clear scope.
- Emergency mode may be misused unless fail-closed behavior remains explicit.
- Promotion evidence may remain underspecified.

## Consequences

- No autonomy escalation occurs without governance approval.
- Autonomy may vary by Organization, Portfolio, Venture, Domain, and Capability.
- Policy Engine enforces autonomy constraints at runtime.

## Enforcement

Autonomy promotion requires approved governance, Evidence, auditability, scope, and rollback path.
