# State Machines

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for state machine architecture.

## Purpose

State machines control lifecycle transitions for opportunities, agents, approvals, production assets, and incidents.

## Existing State Drafts

- Opportunity lifecycle.
- Agent lifecycle.

## State Machine Standard

Every state machine must define:

- States.
- Allowed transitions.
- Transition actor.
- Required evidence.
- Required approval.
- Emitted event.
- Audit requirement.
- Rollback or recovery behavior.

## Rule

No workflow should rely on informal status text when a formal state is required.
