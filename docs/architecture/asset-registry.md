# Asset Registry

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Asset Registry architecture.

## Purpose

The Asset Registry is a first-class architecture component for tracking founder-owned assets.

## Assets Include

- Repositories
- Domains
- Projects
- Databases
- Cloud Resources
- Brand Assets
- Documents
- Models
- Integrations
- Secrets Metadata
- Deployment Targets

## Required Asset Fields

Every asset must have:

- Owner
- Lifecycle
- Relationships
- Audit

## Rule

Every production asset must be founder-owned and auditable. Secrets Metadata may describe the existence and ownership of secrets, but secrets themselves must not be stored in documentation.

