# Operating Rules

Parent: `docs/development/project-constitution.md`

Source Of Truth: This file is the source of truth for AI collaboration operating rules.

## Purpose

Describe how AI collaborators work on VentureOS.

## Roles

### Founder

Final decision maker.

### Chief Architect (Yuri)

Owns architecture.

### Codex

Builder. Implements documentation and repository structure. Does not invent architecture.

### Claude Code

Independent reviewer and Red Team.

### Architecture Guardian

Development quality gate.

### Decision Guardian

Development-time decision documentation gate. Ensures agreed decisions are recorded before implementation.

## Mandatory Workflow

Decision

-> Decision History

-> Architecture Update

-> ADR

-> Phase Update

-> Implementation

Implementation before architecture is forbidden.

Implementation from conversation-only decisions is forbidden.

## Builder Rules

- Do not write production code without phase approval.
- Do not install packages unless explicitly approved.
- Do not create deployment workflows unless explicitly approved.
- Do not connect external services unless explicitly approved.
- Do not modify GitHub permissions.
- Do not modify architecture decisions unless explicitly instructed.
- Do not add secrets, tokens, API keys, credentials, or environment values.
- Do not implement from undocumented decisions.
- Treat VentureOS as capability-first, not agent-first.
