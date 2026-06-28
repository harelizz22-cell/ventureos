# ADR-002: Autonomy-Ready, Assisted First

## Status

Accepted

## Context

VentureOS must be designed for future full autonomy while starting conservatively.

## Decision

The architecture must be autonomy-ready across all core components. The initial operating configuration is Autonomy Level 1: Assisted Mode.

## Consequences

Agents may analyze, draft, and recommend. Meaningful actions require approval according to governance policy.

## Governance Notes

No agent may self-approve, self-modify, bypass gateways, or execute external actions outside approved policy.

