# Execution Reliability

Parent: `docs/architecture/runtime-kernel.md`

Source Of Truth: This file is the source of truth for Execution Reliability architecture.

## Purpose

Define how VentureOS detects, classifies, retries, recovers, escalates, and audits execution failures without weakening Policy, Evidence, Decision, Recovery, or Founder governance.

## Failure Taxonomy

Execution failures must be classified before retry, compensation, rollback, or escalation.

Failure categories include:

- Validation failure
- Policy failure
- Approval failure
- Resource failure
- Timeout failure
- Dependency failure
- Tool failure
- AI Gateway failure
- Event publication failure
- State transition failure
- Idempotency conflict
- Partial execution failure
- Recovery failure
- Compliance-sensitive failure
- Capital-sensitive failure

## Retry Policies

Retry policy must define:

- Whether retry is allowed
- Maximum retry count
- Backoff strategy
- Idempotency requirement
- Retry owner
- Retry audit requirements
- Escalation threshold
- Policy review requirement where meaningful

Retries must not bypass Policy Engine, approval requirements, resource constraints, or compliance gates.

## Idempotency Model

Execution must define an idempotency key or equivalent identity for retryable operations.

Idempotency must prevent duplicate side effects, duplicated Evidence, duplicated Decisions, duplicate payments, duplicate external calls, duplicate asset changes, and duplicate audit confusion.

If idempotency cannot be proven, retry must be blocked or escalated.

## Compensation Model

Compensation is a governed corrective action that offsets or reconciles a completed or partially completed action.

Compensation must preserve audit history. It must not pretend the original action never happened.

Compensation may require Founder approval, delegated approval, compliance review, or capital governance depending on scope.

## Rollback Policy

Rollback attempts to return a system, record, asset, or execution state to a prior safe state.

Rollback must not edit historical Audit, Evidence, or Decision records.

Rollback requires policy evaluation where it affects assets, capital, customers, production state, regulated domains, or irreversible operations.

## Forward Recovery Policy

Forward recovery completes a safe alternative path instead of reverting.

Forward recovery may be preferred when rollback would increase risk, damage audit integrity, break external consistency, or affect customers.

Forward recovery must be governed, auditable, and evidence-supported where meaningful.

## Dead Letter Queue Architecture

Dead Letter Queue is the architectural holding area for failed execution messages, events, or requests that cannot safely complete or retry.

Dead Letter records must include:

- Original request or Event identity
- Scope
- Actor
- Correlation and causation identifiers
- Failure category
- Retry history
- Policy snapshot
- Recovery status
- Escalation status
- Audit references

Dead Letter Queue does not authorize implementation, queue infrastructure, or storage technology.

## Timeout Handling

Timeouts must define:

- Timeout threshold
- Timeout owner
- Retry eligibility
- Approval wait behavior
- Escalation path
- Recovery path
- Audit behavior

Approval timeouts must fail closed unless approved governance defines a safe alternate path.

## Circuit Breaker Architecture

Circuit breakers prevent repeated failure against unstable dependencies, tools, gateways, providers, workflows, or capabilities.

Circuit breaker states may include:

- Closed
- Open
- Half-open
- Manually paused
- Policy-blocked

Opening a circuit breaker must be auditable and may trigger incident creation.

## Retry Backoff Strategy

Retry backoff must reduce repeated pressure on failing dependencies.

Backoff may be immediate, fixed, exponential, jittered, policy-defined, or manually approved depending on failure type.

High-risk, capital-sensitive, compliance-sensitive, or irreversible operations must not use automatic retry unless explicitly governed.

## Partial Failure Handling

Partial failures must preserve:

- Completed steps
- Failed steps
- Pending steps
- Side effects
- Evidence references
- Decision references
- Audit trail
- Recovery options

Partial completion must not be hidden.

## Long-Running Execution Handling

Long-running executions must support:

- Checkpoints
- Heartbeats or progress markers
- Timeout policy
- Pause and resume rules
- Approval renewal where required
- Policy snapshot preservation
- Recovery path
- Audit continuity

## Recovery Checkpoints

Recovery checkpoints identify safe points for retry, compensation, rollback, or forward recovery.

Checkpoints must preserve state, scope, policy context, Event context, and audit references.

## Escalation Model

Escalation is required when:

- Retry limit is reached
- Failure is compliance-sensitive
- Failure is capital-sensitive
- Failure affects production assets
- Failure affects customers
- Policy conflict appears
- Evidence is insufficient
- Recovery fails
- Dead Letter volume exceeds threshold
- Circuit breaker opens repeatedly

Escalation may go to Founder, delegated reviewer, risk reviewer, compliance reviewer, Architecture Guardian, or future incident process.

## Incident Creation Rules

Incident creation is required for:

- Repeated execution failure
- Unsafe partial failure
- Recovery failure
- Data integrity risk
- Audit integrity risk
- Capital-sensitive failure
- Compliance-sensitive failure
- Security-sensitive failure
- Customer-impacting failure
- Circuit breaker threshold breach

## Audit Requirements

Execution reliability records must preserve:

- Failure category
- Retry decision
- Retry count
- Idempotency key
- Compensation decision
- Rollback decision
- Forward recovery decision
- Timeout
- Dead Letter status
- Circuit breaker state
- Incident link
- Recovery evidence
- Policy version or snapshot
- Actor and scope

## Recovery Evidence Requirements

Recovery must cite Evidence where meaningful, including:

- Original failure record
- Execution state
- Event history
- Policy outcome
- Approval outcome
- Impact assessment
- Recovery plan
- Recovery result

## Rule

Execution reliability must preserve governance, auditability, idempotency, recovery safety, and Founder control. Reliability mechanisms must not become a bypass for Policy, Evidence, approval, compliance, or capital governance.

## Placeholder Status

This is architecture documentation only. It does not define queues, services, code, schemas, infrastructure, libraries, integrations, or implementation.
