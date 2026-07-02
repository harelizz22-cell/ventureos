# Execution API

Parent: `docs/architecture/runtime-kernel.md`

Source Of Truth: This file is the source of truth for Execution API architecture.

## Purpose

Define the single entry point for all executions.

## Rule

All Capability execution requests must enter through the Execution API.

No Capability, Agent, Tool, Workflow, Service, or external provider may bypass the Execution API.

## Responsibilities

- Receive execution requests.
- Validate required scope.
- Attach `organization_id`.
- Attach `portfolio_id`.
- Attach `venture_id`.
- Attach `actor_id`.
- Create `correlation_id`.
- Create `causation_id`.
- Attach idempotency key where required.
- Request Policy Engine evaluation.
- Attach policy version or policy snapshot evaluated.
- Pass accepted requests into Runtime Kernel.
- Reject requests with missing governance context.
- Attach approval TTL where approval is required.
- Require approval re-validation before execution start.

## Governance Requirements

The Execution API must reject requests that lack scope, actor identity, Capability reference, policy evaluation path, or audit context.

The Execution API must reject or fail closed requests when policy version, policy snapshot, evaluator consistency, or required governance context cannot be established.

The Execution API must reject retryable or side-effecting requests that require idempotency but lack an idempotency key or equivalent identity.

## Approval Validity Window

Approved execution requests must preserve approval TTL, approval timestamp, approving authority, policy snapshot, scope, and resource assumptions.

Before an approved request starts execution, Execution API or the Runtime Kernel must re-validate:

- Approval TTL.
- Approval authority.
- Policy snapshot or current valid policy requirement.
- Resource availability.
- Token reservation state where AI execution is involved.
- Capital reservation state where capital-sensitive execution is involved.
- Scope and actor context.

If approval expires, resource checks fail after approval, token reservation cannot be verified, capital reservation cannot be verified, or policy context changes materially, execution must not start.

The request must follow a governed cancellation, requeue, or re-evaluation path.

## Founder Unavailability Constraint

Until Founder Unavailability architecture is formally approved, Execution API must fail closed for execution requiring Founder approval when Founder is unavailable. It must not infer delegated approval, auto-approve pending requests, or expand authority under emergency mode.

## Reliability Requirements

Execution API must preserve timeout expectations, retry eligibility, idempotency context, correlation, causation, actor, scope, and policy snapshot so Runtime Kernel can apply Execution Reliability.

## Non-Goals

- No business decision making.
- No investment approval.
- No capital movement.
- No direct Tool Gateway or AI Gateway bypass.

## Placeholder Status

This is architecture documentation only. It does not define API schemas, endpoints, code, or implementation.
