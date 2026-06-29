# Project Roadmap

Parent: `docs/project/ventureos-system-bible.md`

Source Of Truth: This file is the source of truth for engineering roadmap phases.

This is an engineering documentation roadmap. It does not authorize production implementation by itself.

## Architecture Foundation

### Objective

Establish the architecture-first repository foundation and source of truth.

### Inputs

- Founder direction.
- Chief Architect decisions.
- Master architecture document.

### Outputs

- Repository documentation structure.
- Master architecture.
- Initial ADRs.
- Initial phase specifications.

### Dependencies

- Founder approval.
- Chief Architect architecture ownership.

### Acceptance Criteria

- Source of truth exists.
- No production code exists.
- Initial governance rules are documented.

## Governance Core

### Objective

Define enforceable governance rules for VentureOS work and future runtime behavior.

### Inputs

- Master architecture.
- Governance rules.
- Approval model.

### Outputs

- Governance requirements.
- Approval paths.
- Audit requirements.

### Dependencies

- Architecture Foundation.

### Acceptance Criteria

- Required approvals are explicit.
- Governance bypass conditions are documented.
- Audit requirements are reviewable.

## Policy Engine

### Objective

Define how proposed actions are evaluated against governance rules.

### Inputs

- Governance Core documentation.
- Policy Engine rule categories.
- Approval thresholds.

### Outputs

- Policy outcomes.
- Rule categories.
- Testable policy requirements.

### Dependencies

- Governance Core.
- Approved thresholds.

### Acceptance Criteria

- Policy outcomes are defined.
- Deny, allow, and review paths are documented.
- No implementation begins without phase approval.

## Execution Orchestrator

### Objective

Define execution orchestration requirements for capability invocation, approvals, retries, timeouts, failure containment, event coordination, and execution state tracking.

### Inputs

- Master architecture.
- Policy requirements.
- State machine requirements.
- Capability Registry requirements.

### Outputs

- Execution requirements.
- Capability invocation rules.
- Approval workflow definitions.

### Dependencies

- Governance Core.
- Policy Engine.
- Capability Registry.

### Acceptance Criteria

- Execution boundaries are documented.
- External execution remains gateway-controlled.
- State transitions are auditable.

## State Machine

### Objective

Define lifecycle states for opportunities, agents, approvals, assets, and incidents.

### Inputs

- Existing state machine drafts.
- Governance requirements.
- Phase requirements.

### Outputs

- State definitions.
- Transition rules.
- Blocking conditions.

### Dependencies

- Governance Core.
- Workflow Engine.

### Acceptance Criteria

- Required states are named.
- Invalid transitions are documented.
- Build-before-validation is blocked.

## Evidence Engine

### Objective

Define how evidence is captured, evaluated, linked, and reviewed.

### Inputs

- Evidence Ledger specification.
- Decision requirements.
- Research workflow requirements.

### Outputs

- Evidence record requirements.
- Evidence quality requirements.
- Evidence-to-decision linkage rules.

### Dependencies

- Governance Core.
- Decision Engine.

### Acceptance Criteria

- Evidence fields are defined.
- Evidence confidence is explicit.
- Meaningful decisions require evidence links.

## Decision Engine

### Objective

Define how meaningful decisions are proposed, reviewed, approved, recorded, and revisited.

### Inputs

- Decision Ledger specification.
- Evidence requirements.
- Approval model.

### Outputs

- Decision record requirements.
- Approval record requirements.
- Revisit and rollback criteria.

### Dependencies

- Evidence Engine.
- Governance Core.

### Acceptance Criteria

- Decision records are auditable.
- Approval status is explicit.
- Revisit triggers are documented.

## Tool Gateway

### Objective

Define controlled access from agents to external tools.

### Inputs

- Master architecture.
- Tool contract template.
- Security rules.

### Outputs

- Tool access requirements.
- Tool contract requirements.
- Gateway audit requirements.

### Dependencies

- Policy Engine.
- Security principles.

### Acceptance Criteria

- No direct agent tool access is allowed.
- Tool requests are policy-checked.
- Tool actions are auditable.

## AI Gateway

### Objective

Define controlled access from the system to AI providers.

### Inputs

- Master architecture.
- Security rules.
- Prompt and audit requirements.

### Outputs

- AI provider access requirements.
- Prompt safety requirements.
- Gateway audit requirements.

### Dependencies

- Policy Engine.
- Security principles.

### Acceptance Criteria

- No direct provider access bypasses the gateway.
- Secrets are excluded from prompts and logs.
- Provider behavior remains abstracted behind AI Gateway.

## Opportunity Engine

### Objective

Define how business opportunities, external startup investments, acquisitions, and partnerships are captured, assessed, scored, and moved through states.

### Inputs

- Opportunity state machine.
- Evidence requirements.
- Decision requirements.
- Enterprise Value requirements.
- Capital Governance requirements.

### Outputs

- Opportunity record requirements.
- Opportunity Score requirements.
- Investment recommendation inputs.
- Opportunity transition criteria.
- Validation readiness rules.

### Dependencies

- State Machine.
- Evidence Engine.
- Decision Engine.
- Capital Allocation Engine.

### Acceptance Criteria

- Opportunities cannot bypass evidence requirements.
- Investment recommendations cannot bypass governance requirements.
- Opportunity Scores are explainable and evidence-linked.
- State transitions are documented.
- Build proposals require validation readiness.

## Validation Engine

### Objective

Define how opportunities are validated before build work.

### Inputs

- Opportunity Engine requirements.
- Evidence requirements.
- Product validation criteria.

### Outputs

- Validation plan requirements.
- Validation result requirements.
- Build readiness criteria.

### Dependencies

- Opportunity Engine.
- Evidence Engine.

### Acceptance Criteria

- No build begins before validation.
- Validation results are linked to evidence.
- Decisions are recorded before implementation.

## Business Builder

### Objective

Define the approved path from validated opportunity to implementation scope.

### Inputs

- Validation results.
- Decision records.
- Phase approval.

### Outputs

- Implementation scope requirements.
- Asset readiness requirements.
- Review requirements.

### Dependencies

- Validation Engine.
- Decision Engine.
- Asset Registry requirements.

### Acceptance Criteria

- Implementation scope is approved.
- Production asset requirements are known.
- Recovery and monitoring needs are documented.

## Operations Engine

### Objective

Define how launched assets are operated, monitored, improved, and recovered.

### Inputs

- Asset Registry requirements.
- Recovery principles.
- Monitoring requirements.

### Outputs

- Operating requirements.
- Incident requirements.
- Recovery requirements.

### Dependencies

- Business Builder.
- Recovery Architecture.

### Acceptance Criteria

- Assets have owner, backup, rollback, and monitoring plans.
- Incidents have escalation paths.
- Operational decisions are auditable.

## Semi Autonomous

### Objective

Define the controlled transition from Assisted Mode to bounded semi-autonomous execution.

### Inputs

- Governance results.
- Policy Engine requirements.
- Gateway controls.
- Audit evidence.

### Outputs

- Semi-autonomous operating constraints.
- Execution thresholds.
- Monitoring and escalation requirements.

### Dependencies

- Governance Core.
- Policy Engine.
- Tool Gateway.
- AI Gateway.
- Operations Engine.

### Acceptance Criteria

- Autonomy Level 2 constraints are approved.
- Bounded actions are policy-controlled.
- Rollback and escalation requirements are active.

## Fully Autonomous

### Objective

Define requirements for future autonomous company operations under founder governance.

### Inputs

- Semi-autonomous operating history.
- Audit records.
- Governance approval.
- Recovery readiness.

### Outputs

- Autonomous operating requirements.
- Portfolio readiness requirements.
- Governance escalation model.

### Dependencies

- Semi Autonomous.
- Mature evidence, decision, gateway, asset, and recovery systems.

### Acceptance Criteria

- Autonomy Level 3 readiness is explicitly approved.
- Meaningful decisions remain auditable.
- Founder governance remains enforceable.
