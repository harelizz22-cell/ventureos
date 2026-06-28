# Phase 1: System Foundation

Parent: `docs/phases/README.md`

Source Of Truth: This file is the source of truth for Phase 1 System Foundation scope.

## 1. Phase Summary

Phase 1 defines the first real build phase of VentureOS.

The phase objective is to build the system foundation that allows VentureOS to operate as a governed, browser-first, founder-owned autonomous company operating system.

Phase 1 must prepare the platform for future full autonomy while running initially in Autonomy Level 1: Assisted Mode.

Phase 1 is Portfolio-first, Domain-first, and capability-first, not agent-first. AI Agents are implementation details. The Execution Orchestrator owns execution flow. The CEO Agent must not orchestrate the system.

## 2. Phase Goals

- Establish the browser-first system foundation.
- Define the founder-owned account and asset ownership model.
- Prepare durable application data ownership.
- Prepare authentication and founder profile foundations.
- Prepare autonomy setting foundations.
- Prepare governance configuration foundations.
- Prepare Capability Registry and Agent Registry foundations.
- Prepare Decision Ledger, Evidence Ledger, and Audit Log foundations.
- Prepare Execution Orchestrator, Tool Gateway, and AI Gateway placeholders.
- Prepare Founder Operating Console placeholder.
- Prepare Founder Command Center primary screen placeholder.
- Preserve Assisted Mode as the initial operating mode.
- Prevent external execution until approval gates exist.

## 3. Non Goals

- No production launch.
- No autonomous execution.
- No external tool execution.
- No money movement.
- No ads.
- No production customer data.
- No AI provider calls outside a future AI Gateway.
- No external tool calls outside a future Tool Gateway.
- No full database schema.
- No production integration implementation.
- No deployment automation beyond future approved hosting direction.
- No secrets in code, prompts, logs, commits, or documentation.

## 4. Big Plan Context

Phase 1 is the foundation for the long-term VentureOS path:

- Phase 1: System Foundation.
- Phase 2: Governance Core.
- Phase 3: Policy Engine.
- Phase 4: Execution Orchestrator.
- Phase 5: Capability Registry.
- Phase 6: Evidence and Decision Ledgers.
- Phase 7: Founder Operating Console and Founder Command Center.
- Phase 8: Tool Gateway.
- Phase 9: AI Gateway.
- Phase 10: Opportunity Engine.
- Phase 11: Validation Engine.
- Phase 12: Business Builder.
- Phase 13: Operations Engine.
- Phase 14: Semi Autonomous Mode.
- Phase 15: Fully Autonomous Mode.
- Phase 16: Portfolio Mode.

Phase 1 does not complete these future systems. It creates the foundation and boundaries required to build them deliberately.

## 5. System Ownership Model

- GitHub is the source of repository truth.
- Supabase will own durable application data.
- Vercel will host the browser application.
- Trigger.dev will run early execution workflows.
- Future Temporal may replace Trigger.dev for high-durability execution.
- AI providers must be accessed only through AI Gateway.
- External tools must be accessed only through Tool Gateway.
- Founder owns all external accounts and assets.

Ownership must remain founder-controlled. VentureOS must not depend on agent-owned accounts or hidden credentials.

## 6. Runtime Control Model

- Founder Operating Console is the primary interface.
- Founder Command Center is the primary screen.
- Execution Orchestrator controls workflows.
- Governance Core approves or blocks actions.
- Policy Engine evaluates rules.
- Capability Registry defines what the system can do.
- Agent Registry maps capabilities to implementations.
- Decision Ledger records decisions.
- Evidence Ledger records proof.
- Audit Trail records all meaningful action.

The Runtime Control Model follows ADR-004:

Founder -> Organization -> Portfolio -> Venture -> Domain -> Capability -> Workflow -> Execution -> Evidence -> Decision -> Audit

Implementation may be AI, human, API, internal service, or future engine.

## 7. Primary Flow

The first end-to-end system flow is:

Founder signs in
-> Founder profile created
-> Autonomy level set
-> Governance settings configured
-> Capability Registry initialized
-> Policy Engine initialized
-> Execution Orchestrator initialized
-> Founder Operating Console displays system state
-> Founder Command Center presents the primary screen
-> No external execution allowed until approval gates exist

## 8. Phase 1 Scope

Phase 1 includes documentation and skeleton planning for:

- App shell.
- Authentication model.
- Founder profile.
- Autonomy settings.
- Governance config.
- Project state.
- Capability Registry schema planning.
- Agent Registry schema planning.
- Decision Ledger schema planning.
- Evidence Ledger schema planning.
- Audit Log schema planning.
- Execution Orchestrator placeholder.
- Tool Gateway placeholder.
- AI Gateway placeholder.
- Founder Operating Console placeholder.
- Founder Command Center primary screen placeholder.

Schema planning means identifying high-level entities, relationships, and boundaries. It does not authorize full database schema implementation.

## 9. Technology Direction

Approved direction:

- Frontend: Next.js.
- Hosting: Vercel.
- Database: Supabase Postgres.
- Auth: Supabase Auth.
- Workflow: Trigger.dev.
- AI Gateway providers: OpenAI, Claude, Gemini.
- Builder: Codex.
- Reviewer: Claude Code.
- Architecture owner: Yuri.
- Founder approval: required for major decisions.

Technology direction does not authorize integrations, secrets, deployment, or production implementation without approval.

## 10. Initial Data Objects

High-level entities only:

- User.
- Organization.
- Portfolio.
- Venture.
- FounderProfile.
- GovernanceConfig.
- AutonomyLevel.
- Capability.
- CapabilityImplementation.
- AgentContract.
- Decision.
- EvidenceItem.
- AuditEvent.
- ExecutionRun.
- ToolCall.
- AIModelCall.
- Asset.
- Incident.

These are conceptual objects for Phase 1 planning. They are not a complete database schema.

## 11. Required Boundaries

- Frontend cannot enforce business-critical security alone.
- Agents cannot call providers directly.
- No money movement in Phase 1.
- No ads in Phase 1.
- No external tool execution in Phase 1.
- No autonomous actions in Phase 1.
- No production customer data in Phase 1.
- No secrets in code or docs.

## 12. Design Integration

Design source of truth:

`docs/design/`

Phase 1 design direction:

- Browser-first.
- Desktop primary.
- Mobile companion.
- Founder Operating Console.
- Founder Command Center as primary screen.
- Function defines form.
- Stitch is exploration only.
- `docs/design/` is source of truth.

The Phase 1 interface foundation must align with the Founder Operating Console product entry, the Founder Command Center primary screen, and the design documentation foundation.

## 13. Acceptance Criteria

Phase 1 is accepted only when:

- System foundation spec is complete.
- All major boundaries are documented.
- Capability-first model is reflected.
- Execution Orchestrator ownership is clear.
- Founder ownership model is clear.
- No Agent-first orchestration remains.
- No implementation can start without Phase 1 approval.
- Required next documents are identified.

## 14. Required Follow-up Documents

Required follow-up phase documents:

- `docs/phases/phase-2-governance-core.md`
- `docs/phases/phase-3-policy-engine.md`
- `docs/phases/phase-4-execution-orchestrator.md`
- `docs/phases/phase-5-capability-registry.md`

## 15. Risks

- Architecture drift.
- Agent-first regression.
- Governance bypass.
- Premature implementation.
- Provider lock-in.
- Secret leakage.
- Overbuilding.
- Founder control dilution.

## 16. Open Questions

- What specific governance settings are required for the Phase 1 foundation?
- What minimum autonomy settings must exist before Phase 2?
- What founder profile fields are required for the first usable system state?
- What is the minimum acceptable AuditEvent shape for Phase 1 planning?
- What Phase 1 approval process is required before implementation begins?
