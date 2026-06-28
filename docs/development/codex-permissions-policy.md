# Codex Permissions Policy

Parent: `docs/development/project-constitution.md`

Source Of Truth: This file is the source of truth for Codex permission rules.

## Purpose

Define which permissions Codex may request while working on VentureOS.

## Always Allowed

- Write inside repository.
- Modify documentation.
- Create branches.
- Commit.
- Push.
- Pull.
- Read repository.
- Internet only for GitHub operations.

## Founder Approval Required

- Install software.
- External integrations.
- API connections.
- CI/CD changes.
- Infrastructure provisioning.
- Cloud resources.
- Database creation.
- Authentication providers.
- Billing systems.

## Never Allowed

- Store secrets.
- Read private keys.
- Modify GitHub organization settings.
- Change repository ownership.
- Change governance rules.
- Self-approve architectural decisions.
