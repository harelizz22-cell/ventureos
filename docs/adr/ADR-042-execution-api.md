# ADR-042: Execution API

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Execution API decision.

## Status

Accepted

## Context

VentureOS needs a single governed entry point for execution so Capabilities, Agents, Tools, Workflows, Services, and external providers cannot bypass scope, policy, actor identity, correlation, causation, or audit requirements.

## Decision

VentureOS adopts Execution API as the single entry point for all Capability execution requests.

All execution requests must enter through Execution API before Runtime Kernel coordination.

## Alternatives considered

- Allow each implementation mechanism to start execution directly.
- Let Agents call tools or workflows without a single execution entry point.
- Treat Execution API as an implementation detail instead of architecture.

## Rationale

A single execution entry point preserves scope, governance context, Policy Engine evaluation, auditability, and runtime consistency.

## Risks

- Execution API may become too broad unless boundary rules remain clear.
- Missing scope or actor metadata could weaken audit.
- Direct integrations may try to bypass the entry point.

## Consequences

- Execution requests must attach scope, actor, correlation, causation, and policy evaluation context.
- Requests missing governance context must be rejected.
- Runtime Kernel receives only accepted governed execution requests.

## Enforcement

No Capability, Agent, Tool, Workflow, Service, or external provider may bypass Execution API.
