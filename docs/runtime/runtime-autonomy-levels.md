# Runtime Autonomy Levels

Parent: `docs/runtime/README.md`

Source Of Truth: This file is the source of truth for runtime autonomy level behavior.

## Purpose

Define how VentureOS runtime behavior is constrained by autonomy level.

## Scope

This document covers operating behavior for autonomy levels. It does not authorize higher autonomy levels or implementation.

## Non-goals

- No autonomous execution implementation.
- No approval threshold values.
- No production policy engine code.
- No permission escalation.

## Architectural Rules

- Current configuration starts at Autonomy Level 1: Assistant.
- Higher autonomy levels require founder approval.
- Autonomy does not override governance.
- Agents cannot self-approve autonomy expansion.
- Runtime actions must follow policy, evidence, approval, audit, and recovery rules.
- All execution paths must pass through the Policy Engine.
- If the Policy Engine is unavailable, VentureOS fails closed.

## Level 0: Observer

### Purpose

Observe and display system state without recommending or executing actions.

### Allowed Actions

- Display records.
- Display events.
- Display evidence.
- Display decisions.
- Display audit history.

### Blocked Actions

- Recommendations.
- Execution.
- External calls.
- Tool use.
- AI provider calls.
- State changes.

### Approval Requirements

No execution approval applies because execution is not permitted.

### Escalation Rules

Escalate missing governance, missing evidence, or unavailable data to the founder-facing interface.

### Transition Requirements

Founder approval is required to move to Level 1.

### Rollback Behaviour

Rollback returns the system to observation-only mode and blocks all execution.

## Level 1: Assistant

### Purpose

Assist the founder by drafting, summarizing, organizing, and preparing recommendations.

### Allowed Actions

- Draft recommendations.
- Summarize evidence.
- Prepare decision options.
- Request founder decisions.
- Prepare execution proposals.

### Blocked Actions

- Autonomous execution.
- External tool execution.
- Money movement.
- Provider calls outside AI Gateway.
- Tool calls outside Tool Gateway.
- Production asset changes.

### Approval Requirements

Founder approval is required before meaningful action.

### Escalation Rules

Escalate missing evidence, policy uncertainty, high risk, cost exposure, or governance conflict.

### Transition Requirements

Evidence of reliable assistance, governance readiness, and founder approval is required to move to Level 2.

### Rollback Behaviour

Rollback returns to Level 0 or blocks proposed action creation depending on severity.

## Level 2: Approval Required

### Purpose

Allow the system to prepare bounded execution that waits for explicit approval before execution.

### Allowed Actions

- Create execution plans.
- Queue approval requests.
- Validate policy requirements.
- Prepare Tool Gateway or AI Gateway requests.

### Blocked Actions

- Execution without approval.
- Self-approval.
- External calls without gateway approval.
- Actions while Policy Engine is unavailable.

### Approval Requirements

Explicit approval is required for each governed execution.

### Escalation Rules

Escalate denied policy checks, unavailable governance, missing evidence, or cost governance concerns.

### Transition Requirements

Demonstrated policy reliability, audit completeness, recovery readiness, and founder approval are required to move to Level 3.

### Rollback Behaviour

Rollback cancels pending execution and returns to Level 1 or Level 0 depending on incident severity.

## Level 3: Semi Autonomous

### Purpose

Allow bounded execution under explicit policy limits while preserving approval requirements for sensitive actions.

### Allowed Actions

- Execute low-risk bounded workflows.
- Retry within approved policy limits.
- Emit runtime events.
- Trigger recovery workflows when required.

### Blocked Actions

- Actions outside policy.
- Spending above thresholds.
- Agent self-approval.
- Governance bypass.
- Execution while Policy Engine is unavailable.

### Approval Requirements

Approval is required for high-risk, high-cost, external, production, autonomy-expanding, or policy-sensitive actions.

### Escalation Rules

Escalate policy denial, repeated failure, threshold breach, unclear evidence, cost risk, or recovery trigger.

### Transition Requirements

Policy performance, audit history, recovery performance, and founder approval are required to move to Level 4.

### Rollback Behaviour

Rollback suspends autonomous workflow classes and returns to Level 2 for affected capabilities.

## Level 4: Policy Governed Autonomous

### Purpose

Allow autonomous execution for approved capabilities under active policy governance.

### Allowed Actions

- Execute approved capabilities within policy.
- Select interchangeable implementation mechanisms.
- Retry within policy.
- Trigger recovery.
- Emit required events and audit records.

### Blocked Actions

- Policy bypass.
- Governance-unavailable execution.
- Unapproved capability execution.
- Unapproved resource consumption.
- Unapproved provider or tool access.

### Approval Requirements

Approval is required for policy changes, threshold changes, autonomy expansion, high-cost execution, production asset changes, and exception handling outside defined policy.

### Escalation Rules

Escalate policy conflicts, cost breaches, incident triggers, failed recovery, evidence inconsistency, and unclear ownership.

### Transition Requirements

Long-running audit integrity, reliable recovery, cost governance, founder confidence, and explicit approval are required to move to Level 5.

### Rollback Behaviour

Rollback disables affected autonomous policies and returns affected capabilities to Level 2 or Level 3.

## Level 5: Fully Autonomous

### Purpose

Allow broad autonomous operation under founder-governed policy, audit, recovery, and cost controls.

### Allowed Actions

- Execute approved portfolio-level capabilities.
- Coordinate across Organizations, Portfolios, Ventures, Domains, and Capabilities.
- Optimize execution paths within policy.
- Trigger recovery and incident response.

### Blocked Actions

- Founder authority override.
- Policy Engine bypass.
- Governance-unavailable execution.
- Secret exposure.
- Asset ownership dilution.
- Unapproved autonomy expansion.

### Approval Requirements

Founder approval is required for governance changes, authority changes, asset ownership changes, policy boundary changes, high-risk exceptions, and rollback from major incidents.

### Escalation Rules

Escalate material risk, policy ambiguity, evidence conflict, cost anomaly, incident severity, recovery failure, or founder authority impact.

### Transition Requirements

Level 5 requires explicit founder approval, mature audit records, proven recovery, cost governance, policy reliability, and demonstrated lower-level performance.

### Rollback Behaviour

Rollback returns affected Organizations, Portfolios, Ventures, Domains, or Capabilities to the lowest safe autonomy level.

## Open Questions

- What evidence is required to move from Level 1 to Level 2?
- What exact cost thresholds apply at each autonomy level?
- What rollback controls are required for portfolio-level autonomy?
