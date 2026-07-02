# ADR-087: Policy Approval Validity Window

Parent: `docs/architecture/policy-engine.md`

Status: Accepted

## Context

Approved execution may wait in queues while policy, resource, token, or capital context changes.

## Decision

Every approval that can wait before execution must have an approval TTL and must be re-validated before execution start.

## Alternatives

- Treat approvals as valid indefinitely.
- Re-check only policy but not resources.
- Delegate validity to implementation.

## Rationale

Stale approvals can cause execution under outdated governance or resource assumptions.

## Risks

Frequent re-validation may increase operational latency.

## Consequences

Execution API, Execution Scheduler, Resource Coordinator, and Policy Engine must support cancellation, requeue, or re-evaluation when approval context expires or resources change.

## Enforcement

Execution must not start when approval TTL expired, resource checks fail after approval, or policy context materially changes.
