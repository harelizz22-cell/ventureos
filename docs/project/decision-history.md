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
