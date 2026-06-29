# Database Architecture

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for database architecture direction.

## Direction

Supabase Postgres is the preferred future database direction.

## Required Data Domains

- Organizations.
- Portfolios.
- Ventures.
- Business Domains.
- Business Intelligence.
- Governance.
- Evidence.
- Decisions.
- Capabilities.
- Capability implementations.
- Agents.
- Assets.
- Resources.
- Revenue.
- Expenses.
- Venture Timeline.
- Venture Health.
- Venture Digital Twin.
- Value Graph.
- Founder Decision Graph.
- Executive KPIs.
- Events.
- Workflows and executions.
- State.
- Approvals.
- Audit trails.

## Rule

No database schema is approved until phase requirements and data contracts are reviewed.

No global default Venture scope is allowed.

Every future data model for Capability invocation, Execution, Evidence, Decision, Audit, Event, Tool call, AI call, Asset, Cost record, and Investment recommendation must preserve explicit `organization_id`, `portfolio_id`, and `venture_id` scope.

No Domain may read or write another Domain's database, tables, or in-memory state directly.
