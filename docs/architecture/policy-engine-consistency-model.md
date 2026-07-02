# Policy Engine Consistency Model

Parent: `docs/architecture/policy-engine.md`

Source Of Truth: This file is the source of truth for Policy Engine consistency architecture.

## Purpose

Define how VentureOS keeps policy evaluation consistent, auditable, versioned, and fail-closed across runtime execution.

## Policy Versioning

Every policy must have an explicit version.

Policy versions must identify:

- Policy identifier
- Version identifier
- Effective time
- Author or approving authority
- Scope
- Superseded version where applicable
- Related Decision and Audit records where meaningful

## Policy Snapshots

A policy snapshot is the exact policy set evaluated for a governed request.

Every governed execution must record the policy version or policy snapshot used.

Snapshots must preserve:

- Policy versions included
- Evaluation time
- Scope context
- Actor context
- Capability or Workflow context
- Result
- Required approvals
- Conflicts or warnings

## Policy Propagation

Policy changes must propagate in a controlled way.

Until a policy change is effective and visible to the required evaluators, governed execution must use the last valid snapshot or fail closed when consistency cannot be proven.

## Policy Conflict Handling

When policies conflict, the most restrictive valid policy outcome controls unless an approved governance rule defines a stricter conflict resolution path.

Conflict outcomes may include:

- Deny
- Require Founder approval
- Require delegated approval
- Require evidence
- Require risk review
- Require legal/compliance review
- Fail closed

## Policy Evaluation Consistency

Policy evaluation must be deterministic for the same policy snapshot, request context, actor context, scope, and Evidence status.

Policy evaluation must not depend on mutable current-state content unless that state is snapshot-pinned or recorded in the evaluation context.

## Governance Lag Rules

Governance lag is the period between policy change approval and full runtime availability.

During governance lag:

- High-risk execution must fail closed or require explicit approval.
- Runtime components must not assume partial propagation is safe.
- Policy snapshot identity must be recorded.
- Execution may continue only if the active snapshot is valid for the request category.

## Degraded Policy Evaluation

Policy Engine degradation is a governed runtime state where policy evaluation is available but operating below normal confidence, coverage, latency, or freshness expectations.

Degraded mode states:

- Normal: required evaluators, current snapshots, and latency targets are satisfied.
- Degraded Monitor: a non-critical evaluator, dependency, or latency signal is below target, but required policy confidence remains intact.
- Degraded Restricted: reduced evaluator count, stale snapshot risk, or elevated latency exists and only low-risk, reversible, non-capital, non-compliance-sensitive execution may continue.
- Degraded Fail Closed: policy confidence cannot be proven, required evaluators are unavailable, snapshots are stale beyond allowed tolerance, or latency prevents reliable evaluation.

Reduced evaluator count behavior:

- If optional evaluators are unavailable, Policy Engine may continue only when the remaining evaluator set satisfies the degraded-but-acceptable threshold.
- If required evaluators are unavailable, affected execution must fail closed.
- Policy Engine must not substitute a more permissive evaluator for a missing restrictive evaluator.

Stale snapshot behavior:

- Current valid snapshots may continue within an explicit freshness tolerance.
- Stale snapshots may support only low-risk execution when policy allows degraded restricted operation.
- Capital-sensitive, compliance-sensitive, autonomy-expanding, production-asset, cross-Organization, or irreversible execution must fail closed when snapshots are stale.

Elevated latency behavior:

- Elevated latency may pause scheduling, require requeue, or require re-evaluation.
- If latency prevents timely approval validation, execution must not start.
- Emergency mode may restrict execution during latency degradation but must not expand authority.

Thresholds:

- Degraded-but-acceptable threshold means required policy confidence, scope, approval authority, snapshot freshness, and audit record creation remain intact.
- Degraded-to-fail-closed threshold is reached when any required policy input, evaluator, snapshot, authority, approval, or audit path cannot be verified.

Every degraded policy evaluation must create an Audit record identifying degraded state, affected evaluators, snapshot status, latency status, threshold used, outcome, actor, scope, and correlation ID.

## Disagreement Between Evaluators

If two policy evaluators disagree, VentureOS must fail closed for the affected request.

Disagreement must create an auditable policy conflict record that includes:

- Evaluator identities or component identities
- Policy snapshot identifiers
- Input context
- Output differences
- Request scope
- Required escalation

No runtime component may choose the more permissive policy outcome during disagreement.

## Fail-Closed Behavior

VentureOS must fail closed when:

- Policy Engine is unavailable
- Required policy version is missing
- Policy snapshot cannot be produced
- Policy evaluators disagree
- Policy propagation is uncertain for a restricted request
- Policy conflict cannot be resolved
- Required governance context is missing

## Audit Requirements

Every governed request must record:

- Policy version or snapshot used
- Policy evaluation result
- Required approvals
- Denials
- Conflicts
- Fail-closed reason where applicable
- Actor and scope context
- Correlation and causation identifiers

## Rule

Policy consistency is required before execution. Runtime components must not bypass, infer, or locally override Policy Engine outcomes.

## Placeholder Status

This is architecture documentation only. It does not define policy storage, policy language, evaluator code, APIs, services, or implementation.
