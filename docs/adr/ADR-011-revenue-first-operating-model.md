# ADR-011: Revenue-First Operating Model

Parent: `docs/adr/README.md`

Source Of Truth: This file records the earlier revenue-first operating model decision. ADR-015 is the controlling source of truth for Enterprise Value as the primary objective.

## Status

Superseded by ADR-015.

## Context

VentureOS has evolved from building autonomous ventures toward autonomously creating, operating, optimizing, and scaling profitable companies under Founder governance.

## Decision

VentureOS exists to create, operate, optimize, and scale profitable companies autonomously while maintaining Founder governance.

The purpose of VentureOS is measurable value creation. Every subsystem ultimately exists to increase enterprise value.

ADR-015 supersedes this decision where it treats revenue as the primary operating objective. Revenue remains an important KPI, but Enterprise Value is now the primary objective.

## Consequences

- Revenue, profit, cost, growth, and enterprise value become first-class architectural concerns.
- Business Intelligence becomes a Domain.
- Revenue KPIs remain official executive concepts.
- Founder Operating Console must show business health without requiring log inspection.

## Enforcement

Documentation and implementation planning must treat measurable business outcomes as the success measure.
