# ADR-003: Agent Evolution Control

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted agent evolution control decision.

## Status

Accepted

## Context

Future autonomy requires the system to identify missing capabilities and propose new agents without allowing uncontrolled agent proliferation.

## Decision

Agent evolution must follow: Capability Gap Detected -> Agent Proposal -> Risk Review -> Auditor Review -> Founder Approval -> Sandbox Test -> Activation Approval.

## Consequences

The system may recommend and draft agent contracts. It may not activate new agents without founder approval.

## Governance Notes

Agent activation requires auditable evidence, risk review, auditor review, and founder approval.
