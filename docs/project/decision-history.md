# Decision History

Parent: `docs/project/ventureos-system-bible.md`

Source Of Truth: This file is the source of truth for chronological engineering decision history.

| Decision ID | Date | Title | Status | Reason | Related ADR | Impact |
| --- | --- | --- | --- | --- | --- | --- |
| DEC-001 | 2026-06-28 | Establish master architecture source of truth | Accepted | Prevent undocumented implementation drift. | ADR-001 | Architecture changes must update the master source of truth. |
| DEC-002 | 2026-06-28 | Use autonomy-ready architecture with Assisted Mode first | Accepted | Preserve future autonomy while keeping current operation conservative. | ADR-002 | Agents may draft and recommend, but meaningful execution requires approval. |
| DEC-003 | 2026-06-28 | Control agent evolution through governance lifecycle | Accepted | Prevent uncontrolled agent creation or activation. | ADR-003 | New supporting agents require proposal, reviews, founder approval, sandbox testing, and activation approval. |
| DEC-004 | 2026-06-28 | Add Project Operating System foundation | Accepted | Create project continuity, handoff, roadmap, and collaboration rules for documentation work. | None | Adds project operating documentation without changing architecture decisions. |
| DEC-005 | 2026-06-28 | Restructure documentation architecture | Accepted | Create one responsibility and one source of truth per documentation concern. | None | Splits documentation into project, architecture, development, governance, security, recovery, contracts, and project-management concerns. |
| DEC-006 | 2026-06-28 | Apply Architecture Audit #001 fixes | Accepted | Restore ledger specs, create runtime documentation, and add the VentureOS Manifesto after documentation audit findings. | None | Restores Decision Ledger and Evidence Ledger as standalone specs, creates `docs/runtime/`, creates `docs/project/ventureos-manifesto.md`, and sets the next major architecture task. |
| DEC-007 | 2026-06-28 | Create official design documentation foundation | Accepted | Establish one source of truth for VentureOS design direction before UI implementation. | None | Creates `docs/design/`, records Stitch as exploration only, and defines initial design principles, visual identity, color, typography, layout, components, interaction, and accessibility direction. |
| DEC-008 | 2026-06-28 | Record capability-first execution model | Accepted | Ensure agreed architecture decisions are recorded and enforced after Architecture Audit #002. | ADR-004 | Defines VentureOS as a Company Operating System, makes Capability Registry primary, Agent Registry secondary, replaces Workflow Orchestrator terminology with Execution Orchestrator, and adds Decision Guardian. |
| DEC-009 | 2026-06-28 | Create Phase 1 System Foundation specification | Proposed | Define the first real build phase while preserving capability-first execution and Assisted Mode constraints. | ADR-004 | Adds `docs/phases/phase-1-system-foundation.md` and Phase 2-5 placeholders; implementation remains blocked until Phase 1 approval. |
