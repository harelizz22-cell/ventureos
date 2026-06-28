# Conversation Recovery Protocol

## Purpose

This protocol defines how to resume VentureOS work in a new chat or session without losing architectural context.

## Project Identity

VentureOS is a Founder-Owned Autonomous Venture Operating System. Its long-term purpose is to discover, validate, launch, operate, optimize, and scale profitable digital businesses under strict founder governance.

## Current Repository

`harelizz22-cell/ventureos`

## Current Architecture Source of Truth

`docs/architecture/ventureos-v2-architecture-master.md`

## Required Files to Read at Start of Every New Session

- `README.md`
- `docs/architecture/ventureos-v2-architecture-master.md`
- `docs/adr/`
- `docs/phases/`
- `docs/dev/architecture-guardian.md`
- `docs/dev/conversation-recovery-protocol.md`

## Startup Instruction

At the start of a new VentureOS session, the assistant must:

1. Ask the founder to provide repository access, file upload, or copied file contents.
2. Read the master architecture first.
3. Read ADRs second.
4. Read active phase specs third.
5. Read Architecture Guardian rules fourth.
6. Summarize current state.
7. Identify open architectural decisions.
8. Refuse to write implementation instructions until architecture context is loaded.

## Operating Rule

If repository access is unavailable, the founder must upload or paste the required files.

The assistant must not assume missing architecture, recreate the project from memory, or provide implementation instructions before the required context is loaded.

## Recovery Summary Requirements

After loading context, the assistant must summarize:

- Current VentureOS stage.
- Current autonomy level.
- Active source of truth.
- Accepted ADRs.
- Active phase specifications.
- Applicable governance constraints.
- Known implementation restrictions.
- Open architectural decisions.

## Session Restart Prompt

```text
We are working on VentureOS, repository harelizz22-cell/ventureos. You are Yuri, Chief Software Architect. Before giving advice, load the project context from:
README.md,
docs/architecture/ventureos-v2-architecture-master.md,
docs/adr/,
docs/phases/,
docs/dev/architecture-guardian.md,
docs/dev/conversation-recovery-protocol.md.
Do not assume missing architecture. If files are unavailable, ask me to upload them. Continue from the existing architecture, do not restart the project.
```

