# Multi-Tenancy Architecture

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Multi-Tenancy Architecture.

## Purpose

Define how VentureOS supports multiple independent Organizations without data leakage while preserving Portfolio, Venture, User, Agent, Capability, Knowledge, Runtime, Storage, Event, Memory, and AI context isolation.

## Organization Boundary

Organization is the primary tenant boundary.

No Organization may access another Organization's information unless explicitly governed.

Every governed object must carry `organization_id` where applicable.

## Portfolio Boundary

Portfolio belongs to exactly one Organization.

Portfolio data, analytics, Events, Knowledge, and runtime state must not cross Organization boundaries.

Cross-Portfolio intelligence inside an Organization requires Policy Engine authorization and auditability.

## Venture Boundary

Venture belongs to exactly one Portfolio and one Organization.

Raw Venture data must not leak to another Venture unless Policy Engine explicitly allows governed aggregation, comparison, or shared learning.

## User Boundary

Human users must be scoped to authorized Organizations, Portfolios, Ventures, Domains, Capabilities, and roles.

User access must be authenticated and authorized before data, execution, search, analytics, or reasoning access is allowed.

## Agent Boundary

AI Agents are participants and implementation options, not owners of tenant data.

Agents must execute within explicit Organization, Portfolio, Venture, Domain, Capability, policy, and actor scope.

Agents must not retain or reuse one Organization's context in another Organization.

## Capability Boundary

Every Capability belongs to one Domain and executes within explicit scope.

Capability invocation must preserve Organization, Portfolio, Venture, actor, policy, Evidence, Decision, Event, and Audit context where meaningful.

## Knowledge Boundary

Knowledge assets must remain scoped to their owning Organization and lower-level context.

Cross-Venture knowledge use requires Policy Engine authorization, classification, Evidence boundaries, and auditability.

## Runtime Isolation

Runtime execution must preserve tenant scope through Execution API, Policy Engine, Runtime Kernel, Tool Gateway, AI Gateway, Event Architecture, Observability, Recovery, and Audit.

Runtime components must fail closed when tenant scope is missing or ambiguous.

## Storage Isolation

Future storage design must preserve tenant boundaries.

Storage isolation may be logical, physical, or hybrid, but the architecture requirement is no unauthorized cross-tenant access.

This document does not choose storage technology.

## Event Isolation

Events must carry explicit Organization, Portfolio, and Venture scope where applicable.

Event subscribers must not receive Events outside authorized scope.

Cross-tenant Event access is forbidden unless explicitly governed.

## Memory Isolation

Organizational Memory, runtime memory, Agent memory, and Knowledge memory must not cross Organization boundaries without explicit governance.

Memory must preserve source, scope, classification, and auditability.

## AI Context Isolation

AI prompts, retrieval context, tool outputs, summaries, reasoning inputs, and generated outputs must remain tenant-scoped.

AI Gateway must not mix context across Organizations, Portfolios, or Ventures except through explicitly governed aggregate workflows.

## Rule

No Organization may access another Organization's information unless explicitly governed.

## Placeholder Status

This is architecture documentation only. It does not define database schemas, tenancy infrastructure, authentication providers, services, integrations, or implementation.
