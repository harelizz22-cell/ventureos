# Data Ownership Model

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for VentureOS Data Ownership architecture.

## Purpose

Define clear ownership for VentureOS objects so every object has one accountable owner and no data record becomes ownerless, ambiguous, or shared without governance.

## Ownership Rules

Every object must have one clear owner.

Ownership does not automatically imply unrestricted access. Access remains governed by Policy Engine, authorization, scope, Evidence, Decision, and Audit rules.

## Ownership Map

| Object | Owner |
| --- | --- |
| Organization | Founder or approved Organization owner |
| Founder | Founder identity record |
| Portfolio | Owning Organization |
| Venture | Owning Portfolio |
| Evidence | Owning Organization, scoped to Portfolio and Venture where applicable |
| Decision | Authorized deciding actor within owning Organization |
| Knowledge | Owning Organization, scoped to Portfolio, Venture, Domain, or Capability where applicable |
| Organizational Memory | Owning Organization |
| Enterprise Knowledge Graph | Owning Organization |
| Assets | Founder or owning Organization depending on asset class and approved ownership rules |
| AI Outputs | Owning Organization, scoped to actor, Portfolio, Venture, Domain, Capability, and execution context where applicable |
| Runtime Events | Owning Organization, scoped to Portfolio, Venture, Execution, Domain, Capability, and actor where applicable |
| Audit Records | Owning Organization; Audit remains append-only and cannot be edited by owner |

## Founder Ownership

Founder authority remains the highest authority.

Founder ownership of production assets must remain inspectable, recoverable, and auditable.

## Organization Ownership

Organization owns business data, Knowledge, Evidence, runtime state, Events, and audit records unless a stricter asset ownership rule applies.

## Portfolio And Venture Ownership

Portfolio and Venture are scoped ownership containers inside an Organization.

They do not own data outside their Organization boundary.

## Evidence, Decision, And Audit Ownership

Evidence, Decision, and Audit records remain separate concerns.

Evidence supports or challenges claims. Decision records authorized choices. Audit records what happened.

Owners may not rewrite historical Evidence, Decisions, or Audit records.

## Knowledge And Memory Ownership

Knowledge, Organizational Memory, and Enterprise Knowledge Graph records must preserve owner, source, scope, classification, and provenance.

Cross-Venture reuse of Knowledge or Memory requires Policy Engine authorization.

## AI Output Ownership

AI Outputs belong to the Organization and scope that requested them.

AI Outputs do not become Evidence by ownership. Evidence Promotion governance still applies.

## Rule

Every VentureOS object must have one clear owner, and ownership must not bypass authorization, policy, audit, Evidence, or Decision requirements.

## Placeholder Status

This is architecture documentation only. It does not define database schemas, identity providers, access-control implementation, storage implementation, or services.
