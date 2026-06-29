# Resource Domain

Parent: `docs/architecture/domain-model.md`

Source Of Truth: This file is the source of truth for Resource Domain architecture.

## Purpose

The Resource Domain defines resources consumed by VentureOS execution.

## Resources

- Money
- Budgets
- API Credits
- AI Tokens
- Compute
- Storage
- Infrastructure
- API Usage
- Third-party Costs
- Developer Time
- Founder Time
- GitHub
- Domains
- Databases
- Projects
- Secrets
- Future Infrastructure

## Rules

- Every execution consumes Resources.
- Resources are measurable architecture entities.
- Future cost tracking must be supported.
- Resource usage must be auditable when meaningful.
- Secrets are tracked only as metadata; secrets must not be stored in documentation.
- Resource Domain remains the write owner for asset and resource allocation state unless explicitly changed by ADR.

## Placeholder Status

This is an architecture placeholder. It does not define billing integrations, quotas, schemas, or implementation.
