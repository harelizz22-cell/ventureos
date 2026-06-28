# Workflow Orchestrator

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for workflow orchestration architecture.

## Purpose

The Workflow Orchestrator coordinates tasks, approvals, agent handoffs, event handling, and state transitions.

## Direction

Trigger.dev is the preferred first workflow engine. Temporal may be considered later if workflow durability requirements exceed Trigger.dev capabilities.

## Rule

Workflows must enforce governance and state-machine requirements.

