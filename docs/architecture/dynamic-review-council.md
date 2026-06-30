# Dynamic Review Council

Parent: `docs/architecture/strategic-review-domain.md`

Source Of Truth: This file is the source of truth for Dynamic Review Council architecture.

## Purpose

Define how VentureOS assembles a review council for each opportunity.

## Possible Participants

- Market Analyst.
- Technical Architect.
- Financial Analyst.
- Risk Analyst.
- Customer Validation Analyst.
- Strategy Analyst.
- Legal/Compliance Analyst.
- Domain Expert.
- Medical/Regulatory Expert when relevant.
- Security Expert when relevant.
- Investment Analyst when relevant.

## Rule

Council composition is dynamic and depends on opportunity type, risk level, domain, required capital, jurisdiction, and regulatory sensitivity.

Agents are participants only.

They do not self-approve.

They do not bypass Policy Engine.

They do not bypass Evidence requirements.

## Outputs

- Review council composition.
- Participant rationale.
- Required expertise gaps.
- Escalation needs.

## Knowledge And Reasoning Inputs

The Dynamic Review Council may use Enterprise Knowledge Graph relationships, Organizational Memory records, Learning Engine outputs, and Reasoning Engine recommendations to select relevant perspectives and identify expertise gaps.

These inputs are advisory. Council participants remain participants only and do not self-approve, bypass Policy Engine, or bypass Evidence requirements.

## Placeholder Status

This is architecture documentation only. It does not define staffing, agent implementation, prompts, routing logic, or services.
