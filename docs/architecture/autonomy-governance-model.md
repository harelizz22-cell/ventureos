# Autonomy Governance Model

Parent: `docs/runtime/runtime-autonomy-levels.md`

Source Of Truth: This file is the source of truth for autonomy governance architecture.

## Purpose

Define how VentureOS governs autonomy levels, promotion, demotion, safe mode, emergency mode, and partial autonomy across Organization, Portfolio, Venture, Domain, and Capability scope.

## Autonomy Levels

VentureOS uses the autonomy levels defined in `docs/runtime/runtime-autonomy-levels.md`:

- Level 0: Observer
- Level 1: Assistant
- Level 2: Approval Required
- Level 3: Semi Autonomous
- Level 4: Policy Governed Autonomous
- Level 5: Fully Autonomous

The current configuration remains Autonomy Level 1: Assistant.

## Allowed Actions Per Level

Allowed actions must be explicitly defined per level, scope, Domain, Capability, Venture, and Organization where autonomy is active.

Allowed actions may include observation, drafting, recommendations, approval requests, queued execution, bounded execution, recovery triggers, and policy-governed execution depending on level.

## Blocked Actions Per Level

Blocked actions must be explicit.

Blocked actions always include:

- Policy Engine bypass
- Self-approval
- Secret exposure
- Unapproved autonomy escalation
- Governance-unavailable execution
- Unauthorized production asset changes
- Unauthorized capital movement
- Regulated financial activity without legal/compliance approval

## Promotion Rules

Autonomy promotion requires:

- Founder or approved governance approval
- Evidence of successful lower-level operation
- Audit completeness
- Policy Engine readiness
- Recovery readiness
- Cost governance readiness
- Scope definition
- Rollback path

No autonomy escalation may occur without governance approval.

## Demotion Rules

Autonomy must be demoted when:

- Policy violations occur
- Evidence quality is insufficient
- Audit gaps are detected
- Recovery fails
- Cost thresholds are breached
- Compliance uncertainty appears
- Founder or approved governance requires rollback

## Safe Mode

Safe mode reduces runtime capability to conservative behavior.

In safe mode, VentureOS may observe, report, preserve audit, surface pending approvals, and recommend recovery steps. It must not execute higher-risk actions without policy and approval.

## Emergency Mode

Emergency mode is a governed response to severe risk, incident, policy conflict, or recovery event.

Until Founder Unavailability architecture is formally approved, emergency mode may only restrict execution, pause execution, preserve audit, create visibility, or request review.

Emergency mode must not expand authority, grant delegated approval, bypass Founder approval, or approve pending Founder-required actions.

Founder-unavailable state must fail closed. Pending approvals remain pending.

Emergency mode must preserve Founder control, audit, evidence, policy, recovery, and fail-closed behavior.

Emergency mode must not become a bypass for self-approval.

## Partial Autonomy

Autonomy may be configured partially by:

- Organization
- Portfolio
- Venture
- Domain
- Capability

Partial autonomy must preserve explicit scope and must not create global default authority.

## Runtime Enforcement

Policy Engine enforces autonomy rules at runtime.

Runtime Kernel, Execution API, Tool Gateway, AI Gateway, Agents, Workflows, and Capabilities must not locally override autonomy policy.

## Rule

No autonomy escalation is valid without governance approval, Evidence, auditability, scope, and rollback path.

## Placeholder Status

This is architecture documentation only. It does not define permission systems, runtime services, schemas, APIs, or implementation.
