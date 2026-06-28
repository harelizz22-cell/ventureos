# VentureOS

VentureOS is a Founder-Owned Autonomous Venture Operating System. Its purpose is to discover, validate, launch, operate, optimize, and scale profitable digital businesses under strict founder governance.

This repository is currently architecture-first. It contains the source-of-truth architecture, governance rules, decision records, agent contracts, phase plans, and contract templates required before any production implementation begins.

No production application code may be written before architecture approval. Initial operation is Autonomy Level 1: Assisted Mode. The architecture must remain autonomy-ready for future levels.

## Repository Structure

- `docs/architecture/` - master architecture source of truth.
- `docs/adr/` - architecture decision records.
- `docs/phases/` - phase specifications and acceptance criteria.
- `docs/agents/` - agent contracts and MVP agent definitions.
- `docs/contracts/` - API, event, and tool contract templates.
- `docs/governance/` - governance rules, policy model, and approvals.
- `docs/state-machines/` - lifecycle and opportunity state models.
- `docs/security/` - security and secrets principles.
- `docs/recovery/` - recovery and continuity principles.
- `docs/evidence/` - evidence ledger specification.
- `docs/decisions/` - decision ledger specification.
- `docs/diagrams/` - diagram placeholders and conventions.
- `apps/`, `services/`, `agents/`, `workflows/`, `database/`, `infrastructure/`, `tests/` - reserved implementation areas. They must remain non-production until the approved phase plan permits implementation.

## Contribution Workflow

Every meaningful change follows this sequence:

1. Decision
2. Update Architecture
3. ADR
4. Phase Spec
5. Implementation

Changes that affect autonomy, governance, tool access, AI access, spending, security, recovery, or production assets require explicit review before implementation.

