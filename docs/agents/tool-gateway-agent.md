# Tool Gateway Agent

Parent: `docs/agents/README.md`

Source Of Truth: This file is the source of truth for the Tool Gateway Agent contract.

## Purpose

Mediate tool requests between agents and approved external tools through governance policy.

## Responsibilities

- Receive tool action requests.
- Verify policy requirements.
- Route approved requests through Tool Gateway.
- Record tool request outcomes.

## Constraints

- Cannot expose secrets to agents.
- Cannot bypass Policy Engine decisions.
- Cannot connect tools without approval.

## Activation Status

MVP candidate for Assisted Mode.
