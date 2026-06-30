# Runtime Kernel

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for VentureOS Runtime Kernel architecture.

## Purpose

Define VentureOS Runtime Kernel as the execution foundation of the system.

The Runtime Kernel runs the system. It does not make business decisions.

## Architecture Rule

The Runtime Kernel must be dumb in the correct way:

- Enforce policy.
- Coordinate execution.
- Schedule execution.
- Track state.
- Coordinate approvals.
- Coordinate events.
- Manage recovery.
- Coordinate resources.

The Runtime Kernel must not decide whether a business idea is good, whether capital should be allocated, whether an investment should be approved, or what strategy should be created.

## Kernel Service: Execution Coordinator

### Purpose

Coordinate governed execution flow after Execution API intake and Policy Engine evaluation.

### Responsibilities

- Route accepted execution requests to the correct Capability implementation path.
- Coordinate Workflow and Capability execution sequence.
- Coordinate with Approval Coordinator, Event Coordinator, Resource Coordinator, Recovery Manager, and Execution State Tracker.

### Non-Responsibilities

- Business strategy.
- Investment approval.
- Capital allocation decisions.
- Evidence validation.

### Inputs

- Accepted execution request.
- Policy Engine decision.
- Scope context.
- Capability contract.

### Outputs

- Execution start signal.
- Execution coordination state.
- Execution events.
- Failure or recovery trigger.

### Failure Modes

- Missing Policy decision.
- Invalid Capability contract.
- Execution dependency unavailable.
- Policy changes during execution.

### Governance Requirements

- Must preserve policy decision, actor, scope, and approval context.
- Must fail closed when governance is unavailable.

### Related Events

- Execution Started.
- Execution Failed.
- Execution Completed.
- Recovery Started.

### Related Ledgers

- Audit Ledger.
- Decision Ledger where execution follows a Decision.

## Kernel Service: Execution Scheduler

### Purpose

Decide what governed execution runs, waits, pauses, or is deferred.

### Responsibilities

- Queue management.
- Priority handling.
- Fairness across Ventures.
- Resource-aware scheduling.
- Policy-aware scheduling.
- Cost-aware scheduling.
- Rate-limit-aware scheduling.
- Human-approval-aware scheduling.
- Emergency pause support.

### Non-Responsibilities

- Business approval.
- Strategy creation.
- Capital allocation approval.
- Investment approval.

### Inputs

- Governed execution request.
- Queue state.
- Resource availability.
- Policy constraints.
- Approval state.

### Outputs

- Scheduled execution.
- Deferred execution.
- Paused execution.
- Queue state change events.

### Failure Modes

- Queue starvation.
- Resource unavailable.
- Rate limit exceeded.
- Pending approval timeout.

### Governance Requirements

- May schedule only already governed execution requests.
- Must preserve fairness and auditability.

### Related Events

- Execution Queued.
- Execution Scheduled.
- Execution Paused.
- Execution Deferred.

### Related Ledgers

- Audit Ledger.

## Kernel Service: Approval Coordinator

### Purpose

Coordinate approval waiting, timeout, status, and continuation behavior.

### Responsibilities

- Track required approvals.
- Maintain approval waiting state.
- Handle Founder-visible pending decisions.
- Apply timeout rules.
- Route approved, denied, delegated, or expired decisions back to execution flow.

### Non-Responsibilities

- Deciding approval outcome.
- Replacing Founder authority.
- Changing approval policy.

### Inputs

- Policy Engine approval requirement.
- Actor identity.
- Scope context.
- Approval response.

### Outputs

- Approval requested event.
- Approval state update.
- Continuation or denial signal.

### Failure Modes

- Approval timeout.
- Conflicting approval response.
- Missing approval authority.
- Founder unavailable.

### Governance Requirements

- Must preserve who approved, denied, delegated, or failed to respond.
- Must fail closed where approval is required and absent.

### Related Events

- Approval Requested.
- Approval Granted.
- Approval Denied.
- Approval Timed Out.

### Related Ledgers

- Decision Ledger.
- Audit Ledger.

## Kernel Service: Event Coordinator

### Purpose

Coordinate event emission, correlation, causation, ordering, and replay handoff.

### Responsibilities

- Emit required events.
- Preserve event envelope fields.
- Coordinate correlation and causation identifiers.
- Support event ordering and replay requirements.
- Route duplicate or out-of-order events to audit behavior.

### Non-Responsibilities

- Changing business state without execution authority.
- Deciding business meaning of events.
- Rewriting audit history.

### Inputs

- Execution state changes.
- Policy outcomes.
- Approval outcomes.
- Recovery triggers.

### Outputs

- Published events.
- Event audit records.
- Replay coordination signals.

### Failure Modes

- Duplicate event.
- Out-of-order event.
- Missing schema version.
- Event publication failure.

### Governance Requirements

- Must preserve auditability and schema versioning.
- Must not rewrite historical Decisions.

### Related Events

- Audit Recorded.
- State Changed.
- Policy Evaluated.
- Event Replay Requested.

### Related Ledgers

- Audit Ledger.

## Kernel Service: Recovery Manager

### Purpose

Manage governed recovery coordination for failed or unsafe execution.

### Responsibilities

- Route failures to recovery rules.
- Coordinate compensation versus rollback.
- Trigger recovery audit records.
- Escalate recovery failures.
- Coordinate incident and emergency pause behavior where required.

### Non-Responsibilities

- Bypassing Policy Engine.
- Making business decisions.
- Silently undoing audit history.

### Inputs

- Execution failure.
- Policy requirements.
- Recovery plan.
- Incident state.

### Outputs

- Recovery started event.
- Recovery completed event.
- Recovery failed event.
- Escalation request.

### Failure Modes

- Recovery plan missing.
- Recovery action denied by Policy Engine.
- Rollback unavailable.
- Compensation failed.

### Governance Requirements

- Recovery actions pass through Policy Engine where required.
- Recovery audit records are mandatory.

### Related Events

- Recovery Started.
- Recovery Completed.
- Recovery Failed.
- Incident Raised.

### Related Ledgers

- Audit Ledger.
- Decision Ledger where recovery requires approval.

## Kernel Service: Execution State Tracker

### Purpose

Track execution state transitions and make execution status auditable.

### Responsibilities

- Maintain execution state.
- Track state transitions.
- Link state to scope, actor, policy version, approvals, events, and audit records.
- Support Founder Command Center visibility.

### Non-Responsibilities

- Deciding next business action.
- Editing historical audit records.
- Reclassifying evidence.

### Inputs

- Execution request.
- Scheduled state.
- Policy response.
- Approval response.
- Runtime result.

### Outputs

- Execution state record.
- State changed event.
- Founder-visible status.

### Failure Modes

- Missing transition.
- Invalid transition.
- Conflicting state.
- Lost runtime result.

### Governance Requirements

- Every meaningful state transition must be auditable.
- Invalid state transitions must fail closed or require review.

### Related Events

- State Changed.
- Execution Completed.
- Execution Failed.

### Related Ledgers

- Audit Ledger.

## Kernel Service: Resource Coordinator

### Purpose

Coordinate resource availability checks before execution starts.

### Responsibilities

- Budget availability check.
- AI token budget check.
- API quota check.
- Compute availability check.
- Rate limit check.
- Human approval dependency check.
- Capital reservation dependency check.
- Time-window validation.

### Non-Responsibilities

- Approving capital allocation.
- Moving money.
- Selecting business strategy.
- Overriding Cost Governance.

### Inputs

- Execution request.
- Resource requirements.
- Cost Governance constraints.
- Capital reservation state.
- Rate limit state.

### Outputs

- Resource available signal.
- Resource unavailable signal.
- Scheduling constraint.
- Policy or approval escalation.

### Failure Modes

- Budget unavailable.
- Token budget exhausted.
- API quota exhausted.
- Capital reservation conflict.
- Approval dependency missing.

### Governance Requirements

- If required resources are unavailable, execution must not start.
- Resource checks must be auditable where meaningful.

### Related Events

- Resource Checked.
- Resource Blocked.
- Cost Threshold Reached.
- Capital Reservation Conflict.

### Related Ledgers

- Audit Ledger.
- Decision Ledger where resource exception approval is required.

## Placeholder Status

This is architecture documentation only. It does not define runtime services, code, deployment, schemas, or integrations.
