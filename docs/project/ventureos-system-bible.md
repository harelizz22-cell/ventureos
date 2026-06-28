# VentureOS System Bible

Parent: Repository root.

Source Of Truth: This file is the highest-level source of truth for why VentureOS exists and how project documentation is organized.

## Mission

VentureOS exists to help a founder discover, validate, launch, operate, optimize, and scale profitable digital businesses under strict founder governance.

## Vision

VentureOS is a founder-owned autonomous venture operating system designed to move from assisted operation toward governed autonomy without losing auditability, ownership, or human authority.

## Core Philosophy

The system exists to protect founder judgment while increasing operating leverage. Automation is useful only when it is evidence-based, governed, reversible, and owned by the founder.

## Core Principles

- Evidence before action.
- No build before validation.
- Profit before activity.
- Survival before growth.
- Founder owns all assets.
- Every meaningful decision must be auditable.

## Founder Principles

The founder is the final decision maker. The founder owns production assets, approves architecture-changing decisions, and controls autonomy expansion.

## Governance Philosophy

Governance is a design constraint, not an afterthought. The system must prevent unauthorized action, uncontrolled spending, secret exposure, self-approval, and unreviewed autonomy expansion.

## Autonomy Philosophy

VentureOS must be autonomy-ready, but it starts in Assisted Mode. Higher autonomy levels require evidence, governance, review, approval, monitoring, and recovery capability.

## Engineering Philosophy

Engineering work follows architecture. Implementation before architecture approval is forbidden.

## Product Philosophy

Products are built only after validation. Activity is not success. A product decision must connect to evidence, expected profit, risk, and founder approval.

## Asset Ownership

Production assets must be founder-owned and must have an owner, backup plan, rollback plan, and monitoring plan.

## Long-term Vision

The long-term vision is a portfolio-capable venture operating system that can coordinate opportunities, agents, workflows, evidence, decisions, tools, AI providers, production assets, and recovery plans under founder governance.

## Documentation Hierarchy

- `docs/project/` explains why the project exists and what state it is in.
- `docs/project/ventureos-manifesto.md` explains the concise VentureOS philosophy.
- `docs/architecture/` explains how VentureOS is technically structured.
- `docs/adr/` records architecture decisions.
- `docs/phases/` defines approved work phases.
- `docs/agents/` defines agent contracts.
- `docs/governance/` defines governance rules and review requirements.
- `docs/contracts/` defines interface contract formats.
- `docs/contracts/decision-ledger-spec.md` defines the Decision Ledger contract.
- `docs/contracts/evidence-ledger-spec.md` defines the Evidence Ledger contract.
- `docs/runtime/` explains VentureOS behavior while operating.
- `docs/security/` defines security principles.
- `docs/recovery/` defines recovery principles.
- `docs/development/` defines how contributors work.
- `docs/project-management/` tracks planning, risk, and delivery management.

## Source Of Truth Hierarchy

1. Founder decision.
2. Chief Architect architecture direction.
3. `docs/project/ventureos-system-bible.md`
4. `docs/project/ventureos-manifesto.md`
5. `docs/architecture/ventureos-architecture.md`
6. Accepted ADRs in `docs/adr/`
7. Active phase documents in `docs/phases/`
8. Concern-specific source documents.

When documents conflict, the higher item in this hierarchy controls until corrected.

## How AI Participates In The Project

AI collaborators participate through assigned roles. Codex builds documentation and repository structure. Claude Code or equivalent reviewers provide independent review. The Architecture Guardian reviews compliance. AI does not own architecture, approve itself, override the Chief Architect, or replace founder approval.

## Explicit Non Goals

- No production code in documentation foundation work.
- No implementation details in this file.
- No database schema in this file.
- No APIs in this file.
- No component design in this file.
- No secrets, tokens, credentials, or environment values.
- No external service connection.
- No deployment workflow creation without approval.

## Repository Rules

- Keep one source of truth per concern.
- Avoid duplicated rules across documents.
- Link to parent documents instead of repeating full content.
- Keep architecture decisions in ADRs.
- Keep project process in `docs/development/`.
- Keep project planning in `docs/project-management/`.
