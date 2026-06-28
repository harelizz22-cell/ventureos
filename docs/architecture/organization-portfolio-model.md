# Organization And Portfolio Model

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the source of truth for Organization and Portfolio architecture.

## Purpose

Define Organization and Portfolio as first-class architectural entities.

## Hierarchy

Founder
-> Organization
-> Portfolio
-> Venture

## Authority Versus Business Structure

Authority hierarchy:

Founder -> Organization -> Portfolio -> Venture

Business hierarchy begins at Organization.

Founder remains the highest authority but is not a business entity.

## Organization

An Organization is the owned operating boundary for portfolios, ventures, assets, identities, resources, policies, evidence, decisions, and audit.

## Portfolio

A Portfolio groups ventures under a shared operating and governance context.

## Portfolio-First Rule

VentureOS is Portfolio-first. A single venture is simply a portfolio containing one venture.

The system must never assume a single company. Every future capability must be multi-venture aware.

## Long-Term Requirement

The architecture must support multiple Organizations, multiple Portfolios, and hundreds of Ventures without redesign.
