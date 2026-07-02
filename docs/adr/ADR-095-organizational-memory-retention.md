# ADR-095: Organizational Memory Retention

Parent: `docs/architecture/organizational-memory.md`

Status: Accepted

## Context

Organizational Memory needs retention classification so historical or archived context is not mistaken for current operational memory.

## Decision

Adopt active memory, historical memory, archived memory, retention policy, archival model, and operational versus historical classification.

## Alternatives

- Treat all memory as equally current.
- Archive memory without graph classification.
- Leave retention to storage implementation.

## Rationale

Memory retention protects reasoning quality, auditability, and long-term learning.

## Risks

Incorrect classification may hide useful context or surface stale context.

## Consequences

Organizational Memory and Enterprise Knowledge Graph must expose memory status and archival context.

## Enforcement

Archived memory must not be used as current operational context unless explicitly requested, classified, and governed.
