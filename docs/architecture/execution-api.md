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
- Request Policy Engine evaluation.
- Pass accepted requests into Runtime Kernel.
- Reject requests with missing governance context.

## Governance Requirements

The Execution API must reject requests that lack scope, actor identity, Capability reference, policy evaluation path, or audit context.

## Non-Goals

- No business decision making.
- No investment approval.
- No capital movement.
- No direct Tool Gateway or AI Gateway bypass.

## Placeholder Status

This is architecture documentation only. It does not define API schemas, endpoints, code, or implementation.
