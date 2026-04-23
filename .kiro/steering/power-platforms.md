---
inclusion: auto
---

# Power Platform Standards

When working on any Power Platform project (Power Pages, Power Apps, Power Automate, Dataverse):

- Follow the architecture and patterns in #[[file:.agent/skills/build/power-platform-skills-main/CLAUDE.md]]
- Follow the agent conventions in #[[file:.agent/skills/build/power-platform-skills-main/AGENTS.md]]
- For Power Apps code components, follow #[[file:.agent/skills/build/power-apps-code-apps-skill-main/README.md]]

## Core Rules

- Always validate against Dataverse schema before creating or modifying tables
- Use environment variables for configuration, never hardcode connection strings or URLs
- Follow the principle of least privilege for security roles and web roles
- Use solution-aware development — all customizations belong in a solution
- Test OData queries before embedding them in production code
- For Power Pages sites, always include accessibility checks and responsive design
- Run validation scripts when available (check skill `scripts/` folders)

## Naming Conventions

- Tables: PascalCase with publisher prefix (e.g., `contoso_ProjectTask`)
- Columns: PascalCase descriptive names (e.g., `EstimatedCompletionDate`)
- Flows: Verb-noun format (e.g., `Send Approval Notification`)
- Web roles: Descriptive, role-based names (e.g., `Authenticated Portal User`)
