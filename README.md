# VentureOS

Parent: Repository root.

Source Of Truth: `docs/project/ventureos-system-bible.md`

VentureOS is a Founder-Owned Autonomous Company Operating System. It exists to maximize long-term Enterprise Value while preserving Founder control, governance, transparency, and capital discipline.

This repository is currently architecture-first. It contains the documentation architecture, governance rules, decision records, agent contracts, phase plans, and contract templates required before any production implementation begins.

No production application code may be written before architecture approval. Initial operation is Autonomy Level 1: Assisted Mode. The architecture must remain autonomy-ready for future levels.

## Repository Structure

- `docs/project/` - project identity, system bible, current context, roadmap, handoff, and decision history.
- `docs/architecture/` - technical architecture index and concern-specific architecture sources of truth.
- `docs/adr/` - architecture decision records.
- `docs/phases/` - phase specifications and acceptance criteria.
- `docs/agents/` - agent contracts and MVP agent definitions.
- `docs/contracts/` - API, event, tool, agent, Decision Ledger, and Evidence Ledger contract/spec documents.
- `docs/governance/` - governance rules, approval model, risk model, evidence rules, cost governance, and compliance rules.
- `docs/runtime/` - VentureOS behavior while the system is operating.
- `docs/design/` - official product design direction, design principles, visual identity, interaction model, and component rules.
- `docs/security/` - security and secrets principles.
- `docs/recovery/` - recovery, backup, rollback, and incident response strategy.
- `docs/diagrams/` - diagram placeholders and conventions.
- `docs/development/` - engineering collaboration, review, branch, PR, and permission rules.
- `docs/project-management/` - milestones, release planning, focus, future ideas, technical debt, and known risks.
- `apps/`, `services/`, `agents/`, `workflows/`, `database/`, `infrastructure/`, `tests/` - reserved implementation areas. They must remain non-production until the approved phase plan permits implementation.

## Documentation Hierarchy

The highest-level project document is `docs/project/ventureos-system-bible.md`.

Use this rule for where information belongs:

- Why VentureOS exists belongs in `docs/project/ventureos-system-bible.md` and the concise philosophy belongs in `docs/project/ventureos-manifesto.md`.
- How VentureOS is technically structured belongs in `docs/architecture/`, starting with `docs/architecture/context-map.md`.
- Enterprise Value architecture belongs in `docs/architecture/enterprise-value-engine.md`.
- Capital allocation architecture belongs in `docs/architecture/capital-allocation-engine.md` and capital governance belongs in `docs/governance/capital-governance.md`.
- Investment recommendation architecture belongs in `docs/architecture/investment-engine.md`.
- Opportunity scoring belongs in `docs/architecture/opportunity-score.md`.
- Venture lifecycle investment gates belong in `docs/architecture/stage-gate-investment-model.md`.
- How VentureOS behaves during execution belongs in `docs/runtime/`.
- How VentureOS should look, feel, and behave as an interface belongs in `docs/design/`.
- Architecture decisions belong in `docs/adr/`.
- Approved work boundaries belong in `docs/phases/`.
- Agent responsibilities belong in `docs/agents/`.
- Governance rules belong in `docs/governance/`.
- Interface formats and ledger specs belong in `docs/contracts/`, including `docs/contracts/decision-ledger-spec.md`, `docs/contracts/evidence-ledger-spec.md`, and `docs/contracts/audit-ledger-spec.md`.
- Security rules belong in `docs/security/`.
- Recovery rules belong in `docs/recovery/`.
- Engineering team process belongs in `docs/development/`.
- Planning and delivery tracking belongs in `docs/project-management/`.

Each document must have one responsibility, identify its parent document, and identify its source of truth.

## Contribution Workflow

Every meaningful change follows this sequence:

1. Decision
2. Update Architecture
3. ADR
4. Phase Spec
5. Implementation

Changes that affect autonomy, governance, tool access, AI access, spending, security, recovery, or production assets require explicit review before implementation.

## Development Workflow

VentureOS development follows this governance path:

Founder

-> Chief Architect

-> Architecture

-> ADR

-> Phase Specification

-> Codex Implementation

-> Architecture Guardian Review

-> Claude Review

-> Founder Approval

-> Merge

Implementation before architecture approval is forbidden.
