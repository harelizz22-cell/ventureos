# ADR-097: Founder Unavailability Fail Closed

Parent: `docs/architecture/runtime-kernel.md`

Status: Accepted

## Context

Founder unavailability could otherwise be misused as a reason to delegate authority or proceed without approval.

## Decision

Until Founder Unavailability architecture is formally approved, founder-unavailable state fails closed, no delegated approval is allowed, pending approvals remain pending, and emergency mode may restrict execution but not expand authority.

## Alternatives

- Allow emergency delegated approval.
- Allow automatic approval after timeout.
- Leave behavior undefined until a future architecture.

## Rationale

Founder control is a non-negotiable architecture principle.

## Risks

Important work may remain pending during Founder unavailability.

## Consequences

Runtime Kernel, Execution API, Policy Engine, and Autonomy Governance must fail closed for Founder-required approvals when Founder is unavailable.

## Enforcement

No component may infer, delegate, or auto-approve Founder authority until a formal Founder Unavailability architecture is approved.
