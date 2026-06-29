# Runtime Documentation

Parent: `docs/project/ventureos-system-bible.md`

Source Of Truth: This file is the source of truth for the runtime documentation area.

## Purpose

Runtime docs describe VentureOS behavior while the system is operating.

## Scope

Runtime docs explain how VentureOS itself behaves during execution. Development docs explain how the engineering team works.

## Separation From Development Docs

Runtime docs are separate from development docs. Development docs live in `docs/development/` and define engineering collaboration, review, permissions, branching, and definition of done.

Runtime docs live in `docs/runtime/` and define operating behavior such as runtime agent lifecycle, runtime memory, runtime events, tool execution, and autonomy levels.

## Runtime Documents

- `docs/runtime/runtime-agent-lifecycle.md`
- `docs/runtime/runtime-memory.md`
- `docs/runtime/runtime-events.md`
- `docs/runtime/runtime-tool-execution.md`
- `docs/runtime/runtime-autonomy-levels.md`

## Startup Fail-Closed Rule

At startup, Execution Orchestrator must not accept execution requests until Policy Engine health is confirmed.

If Policy Engine becomes unavailable, new execution must stop fail-closed.
