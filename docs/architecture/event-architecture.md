# Event Architecture

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for event architecture.

## Purpose

VentureOS adopts Event-first runtime. Events represent meaningful system facts that other components may observe.

Everything meaningful emits events. Future systems must subscribe to events instead of tightly coupling services.

## Event Categories

- Evidence recorded.
- Organization Created.
- Portfolio Created.
- Venture Created.
- Idea Created.
- Research Started.
- Validation Started.
- Validation Completed.
- Founder Approved.
- Development Started.
- Infrastructure Ready.
- Landing Page Published.
- Traffic Started.
- First Lead.
- First Customer.
- Revenue Generated.
- Scaling Started.
- Capability Registered.
- Capability Executed.
- Decision proposed.
- Decision Approved.
- Approval requested.
- Approval granted.
- Policy denied.
- Policy Violated.
- Workflow started.
- Workflow Completed.
- State changed.
- Asset registered.
- Incident opened.
- Incident Raised.
- Recovery Started.
- Audit Recorded.
- Execution Failed.
- Execution Retried.

## Event Envelope Standard

Every Event must use a standard envelope with:

- `event_id`
- `event_type`
- `occurred_at`
- `source_domain`
- `source_component`
- `organization_id`
- `portfolio_id`
- `venture_id`
- `actor_id`
- `correlation_id`
- `causation_id`
- `payload`
- `schema_version`

## Scope Rule

Every Event must carry explicit `organization_id`, `portfolio_id`, and `venture_id` scope.

No global default Venture scope is allowed.

## Versioning Rule

Event payloads must be versioned.

Breaking Event payload changes require a new version, migration plan, ADR if architecturally significant, and compatibility window where required.

## Rule

Event contracts must be documented in `docs/contracts/event-contract-template.md` before implementation.

Meaningful execution, evidence, decision, policy, asset, recovery, and audit behavior must emit events.

Every major system event must be visible in the Venture Timeline.
