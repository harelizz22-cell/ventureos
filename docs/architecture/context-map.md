# VentureOS Context Map

Parent: `docs/architecture/ventureos-architecture.md`

Source Of Truth: This file is the first architecture document every new contributor should read.

## Purpose

Explain the VentureOS architecture in one page.

## Core Identity

VentureOS is a Company Operating System. AI is not the product. AI is one execution option.

VentureOS is Portfolio-first and capability-first. A single venture is a portfolio containing one venture.

## Architecture Hierarchy

Founder
-> Organization
-> Portfolio
-> Venture
-> Domain
-> Capability
-> Workflow
-> Execution
-> Evidence
-> Decision
-> Audit

## Execution Model

Capabilities are invoked through the Execution Orchestrator. Implementation may be AI, human, API, internal service, or future engine.

## Runtime Model

Everything meaningful emits events. Future systems must subscribe to events instead of tightly coupling services.

## Product Entry

The primary product entry is the Founder Operating Console. The primary screen is the Founder Command Center.

## Long-Term Scale Target

VentureOS must be able to manage multiple Organizations, multiple Portfolios, hundreds of Ventures, thousands of Capabilities, and millions of Events without architectural redesign.

