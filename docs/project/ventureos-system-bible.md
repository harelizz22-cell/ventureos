# VentureOS System Bible

Parent: Repository root.

Source Of Truth: This file is the highest-level source of truth for why VentureOS exists and how project documentation is organized.

## Mission

VentureOS exists to maximize long-term Enterprise Value while preserving Founder control, governance, transparency, and capital discipline.

Revenue is an important KPI. Enterprise Value is the primary objective.

The purpose of VentureOS is measurable value creation. Every subsystem ultimately exists to increase Enterprise Value through evidence-backed decisions, governed execution, auditable learning, and capital discipline.

## Vision

VentureOS is a founder-owned autonomous company operating system designed to move from assisted operation toward governed autonomy without losing auditability, ownership, or human authority.

It is designed to become a venture studio, capital allocation system, and future investor marketplace, but only through approved legal/compliance structure and Founder governance.

## Core Philosophy

The system exists to protect founder judgment while increasing measurable enterprise value across Organizations, Portfolios, and Ventures. Automation is useful only when it is evidence-based, governed, reversible, owned by the founder, and tied to business outcomes.

VentureOS is different from an AI agent app because AI is only one implementation option. The product identity is the governed operating system: Thesis, Hypothesis, Evidence, Policy, Decision, Audit, Capital Allocation, Funding Readiness, and Enterprise Value.

## Core Principles

The official non-negotiable architecture principles are defined in `docs/architecture/architecture-principles.md`.

- Evidence before action.
- Hypothesis before validation.
- Thesis before capital allocation.
- No build before validation.
- Enterprise Value before revenue.
- Capital discipline before scale.
- Diversification before concentration.
- Learning before repetition.
- Profit before activity.
- Outcomes before tasks.
- Enterprise value before technical activity.
- Survival before growth.
- Founder owns all assets.
- Every meaningful decision must be auditable.

## Founder Principles

The founder is the final decision maker. The founder owns production assets, approves architecture-changing decisions, and controls autonomy expansion.

Authority hierarchy is Founder -> Organization -> Portfolio -> Venture. Business hierarchy begins at Organization. Founder remains the highest authority but is not a business entity.

## Governance Philosophy

Governance is a design constraint, not an afterthought. The system must prevent unauthorized action, uncontrolled spending, secret exposure, self-approval, and unreviewed autonomy expansion.

All execution paths must pass through the Policy Engine. If governance is unavailable, VentureOS fails closed and execution is not permitted.

Policy evaluation must be versioned, snapshot-aware, auditable, and fail-closed when consistency cannot be proven.

Future investor marketplace and funding capabilities are governance-gated, compliance-gated, evidence-based, not enabled in MVP, and not autonomous money movement.

## Autonomy Philosophy

VentureOS must be autonomy-ready, but it starts in Assisted Mode. Higher autonomy levels require evidence, governance, review, approval, monitoring, and recovery capability.

No autonomy escalation may occur without governance approval, explicit scope, auditability, and rollback path.

## Engineering Philosophy

Engineering work follows architecture. Implementation before architecture approval is forbidden.

## Product Philosophy

Products are built only after validation. Activity is not success. A product decision must connect to evidence, expected profit, risk, founder approval, and measurable business outcome.

Every Venture starts as an explicit business hypothesis. No Venture may move from idea to validation without an approved hypothesis.

Every Venture, external investment, acquisition, or capital allocation must pass Thesis alignment review before proceeding.

Learning from outcomes must be evidence-backed and auditable.

Organizational intelligence must be durable and governed. Enterprise Knowledge Graph connects approved knowledge and architecture entities. Organizational Memory preserves what happened and what VentureOS remembers. Reasoning Engine produces explainable recommendations from approved knowledge, memory, Evidence, and context. These concerns do not replace Learning Engine and do not make autonomous decisions.

Future funding and investor marketplace architecture may explain opportunities, readiness, risk, evidence, and milestone-based capital plans to qualified audiences only after legal/compliance review. VentureOS must not claim it can legally raise funds, sell securities, hold investor money, or execute investments without the appropriate legal entity, licensing, jurisdictional review, and compliance framework.

No guaranteed return language is allowed.

## Asset Ownership

Production assets must be founder-owned and must have an owner, backup plan, rollback plan, and monitoring plan.

## Long-term Vision

The long-term vision is an Enterprise Value-first, outcome-driven, Portfolio-first company operating system that can manage multiple Organizations, multiple Portfolios, hundreds of Ventures, thousands of Capabilities, and millions of Events without architectural redesign.

AI is not the product. AI is one implementation option for capabilities.

## Documentation Hierarchy

- `docs/project/` explains why the project exists and what state it is in.
- `docs/project/ventureos-manifesto.md` explains the concise VentureOS philosophy.
- `docs/architecture/` explains how VentureOS is technically structured.
- `docs/architecture/context-map.md` is the first architecture document every new contributor should read.
- `docs/adr/` records architecture decisions.
- `docs/phases/` defines approved work phases.
- `docs/agents/` defines agent contracts.
- `docs/governance/` defines governance rules and review requirements.
- `docs/governance/cost-governance.md` defines cost as an architectural governance concern.
- `docs/contracts/` defines interface contract formats.
- `docs/contracts/decision-ledger-spec.md` defines the Decision Ledger contract.
- `docs/contracts/evidence-ledger-spec.md` defines the Evidence Ledger contract.
- `docs/contracts/audit-ledger-spec.md` defines the Audit Ledger contract.
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

In VentureOS runtime architecture, AI is an implementation option, not the product identity.

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
