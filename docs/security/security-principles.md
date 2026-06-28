# Security Principles

- Secrets must never appear in prompts, logs, commits, or documentation.
- Agents receive scoped capabilities, not raw credentials.
- External tool access must route through Tool Gateway.
- AI model access must route through AI Gateway.
- Production assets require monitoring and recovery plans.
- Security-sensitive changes require review before implementation.

