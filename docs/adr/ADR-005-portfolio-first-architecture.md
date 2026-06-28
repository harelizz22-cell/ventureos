# ADR-005: Portfolio-First Architecture

Parent: `docs/adr/README.md`

Source Of Truth: This file is the source of truth for the accepted Portfolio-first architecture decision.

## Status

Accepted

## Context

VentureOS must support more than one venture over time. Assuming a single company would force future redesign.

## Decision

VentureOS is Portfolio-first. A single venture is simply a portfolio containing one venture.

The system must never assume a single company. Every future capability must be multi-venture aware.

## Consequences

- Portfolio becomes a first-class architecture concept.
- Venture is scoped within Portfolio.
- Future capabilities must be evaluated for multi-venture awareness.
- Phase specifications must avoid single-venture assumptions.

## Enforcement

Architecture Guardian and Decision Guardian must flag single-company assumptions unless explicitly scoped and approved.

