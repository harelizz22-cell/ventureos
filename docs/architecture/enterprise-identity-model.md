# Enterprise Identity Model

Parent: `docs/architecture/identity-domain.md`

Source Of Truth: This file is the source of truth for Enterprise Identity Model architecture.

## Purpose

Define enterprise-scale identities for VentureOS and clarify authentication versus authorization responsibilities.

## Identity Types

VentureOS must define identities for:

- Founder
- Organization
- Portfolio
- Venture
- Human Users
- AI Agents
- Runtime Services
- External Systems
- Investors (future)
- Partners (future)

## Founder Identity

Founder is the highest authority identity.

Founder identity may approve architecture-changing decisions, autonomy expansion, production asset ownership, and sensitive governance decisions.

## Organization Identity

Organization identity is the primary tenant identity.

Organization identity anchors data ownership, tenant isolation, policy scope, audit scope, and future customer boundaries.

## Portfolio And Venture Identity

Portfolio and Venture identities provide business hierarchy and scope.

Every governed execution, Evidence record, Decision record, Audit record, Event, AI call, Tool call, Asset, Cost record, and investment recommendation must carry explicit scope where applicable.

## Human User Identity

Human users require authentication and authorization.

Human access must be scoped by Organization, Portfolio, Venture, Domain, Capability, role, policy, and approval where required.

## AI Agent Identity

AI Agents must have explicit identity, role, permissions, owning scope, and Capability boundaries.

Agents cannot self-approve, expand their own permissions, or cross tenant boundaries.

## Runtime Service Identity

Runtime Services require service identity for audit, policy evaluation, Event emission, recovery, and least-privilege access.

Runtime Service identity does not replace actor identity.

## External System Identity

External Systems must be represented with explicit identity, owner, scope, permissions, contract, and audit requirements before integration.

No integrations are approved by this document.

## Investor Identity

Investor identity is future-phase only.

Investor identity must remain compliance-gated and must not authorize securities activity, investor access, or fundraising without legal/compliance approval.

## Partner Identity

Partner identity is future-phase only.

Partner access must be scoped, governed, auditable, and revocable.

## Authentication Versus Authorization

Authentication verifies identity.

Authorization determines what the identity may see, do, search, reason over, execute, approve, recover, or export.

Policy Engine remains the runtime enforcement point for governed authorization.

## Rule

Identity must be explicit, scoped, auditable, and authorization-bound. Authentication alone never grants access or execution authority.

## Placeholder Status

This is architecture documentation only. It does not define identity providers, SSO, accounts, schemas, IAM policies, services, integrations, or implementation.
