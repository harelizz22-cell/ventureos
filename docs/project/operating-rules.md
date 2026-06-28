# Operating Rules

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

## Mandatory Workflow

Decision

-> Architecture Update

-> ADR

-> Phase Update

-> Implementation

Implementation before architecture is forbidden.

## Builder Rules

- Do not write production code without phase approval.
- Do not install packages unless explicitly approved.
- Do not create deployment workflows unless explicitly approved.
- Do not connect external services unless explicitly approved.
- Do not modify GitHub permissions.
- Do not modify architecture decisions unless explicitly instructed.
- Do not add secrets, tokens, API keys, credentials, or environment values.

