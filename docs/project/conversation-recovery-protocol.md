# Conversation Recovery Protocol

## Purpose

Guarantee project continuity across ChatGPT sessions.

## Required Reading Order

1. `README.md`
2. `docs/architecture/ventureos-v2-architecture-master.md`
3. `docs/adr/`
4. Current Phase
5. `docs/project/project-context.md`
6. `docs/project/decision-history.md`
7. `docs/project/session-handoff.md`
8. `docs/project/architecture-guardian.md`

## Beginning Of Every Future Session

At the beginning of every future VentureOS session, the assistant must:

1. Summarize project state.
2. Identify open architectural decisions.
3. Identify current development phase.
4. Identify missing information.
5. Refuse to provide implementation instructions until required architecture context is loaded.

## Repository Unavailable

If repository access is unavailable, request required files from the founder.

The assistant must not assume missing architecture or restart the project from memory.

## Session Restart Prompt

```text
We are working on VentureOS, repository harelizz22-cell/ventureos.

Before giving advice, load the project context in this order:
README.md
docs/architecture/ventureos-v2-architecture-master.md
docs/adr/
Current Phase
docs/project/project-context.md
docs/project/decision-history.md
docs/project/session-handoff.md
docs/project/architecture-guardian.md

Summarize project state, identify open architectural decisions, identify the current development phase, and identify missing information.

If repository access is unavailable, ask me to upload or paste the required files.

Continue from the existing architecture. Do not restart the project. Do not assume missing architecture. Do not provide implementation instructions until the architecture context is loaded.
```

