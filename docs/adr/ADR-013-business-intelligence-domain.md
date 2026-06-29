# ADR-013: Business Intelligence Domain

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Business Intelligence Domain decision.

## Status

Accepted

## Context

Portfolio-first operation requires cross-venture insight, revenue intelligence, cost intelligence, forecasting, KPI aggregation, and executive reporting.

## Decision

Business Intelligence is added as a Business Domain.

It owns business analytics, revenue intelligence, cost intelligence, growth intelligence, forecasting, KPI aggregation, strategic recommendations, portfolio insights, cross-venture comparison, and executive reporting.

## Consequences

- Business Intelligence becomes part of the Domain model.
- Portfolio Intelligence becomes an architectural concern.
- Executive KPIs become first-class concepts.

## Enforcement

Future reporting, forecasting, and portfolio insight capabilities must identify Business Intelligence as the owning Domain unless another Domain is explicitly approved.

