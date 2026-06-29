# Identity Domain

Parent: `docs/architecture/domain-model.md`

Source Of Truth: This file is the source of truth for Identity Domain architecture.

## Purpose

The Identity Domain defines supported identity types and identity boundaries.

## Supported Identities

- Founder
- Employee
- Agent
- AI Worker
- Reviewer
- Auditor
- Service Account
- External Partner
- API Identity

## Agent Identity Rule

Agents are first-class identities in the Identity Domain.

Agents are not anonymous code acting on behalf of a human.

Every Agent must have:

- Identity record.
- Allowed scope.
- Autonomy ceiling.
- Capability permissions.
- Audit attribution.

## Rule

Future identities must extend this model. Identity must not be reduced to authentication provider implementation.

## Placeholder Status

This is an architecture placeholder. It does not define auth schema, roles, permissions, or provider implementation.
