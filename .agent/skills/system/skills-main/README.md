> **Note:** This repository contains example skills originally created by Anthropic for Claude, adapted for cross-platform use. For information about the Agent Skills standard, see [agentskills.io](http://agentskills.io).

# Skills

Skills are folders of instructions, scripts, and resources that AI assistants load dynamically to improve performance on specialized tasks. Skills teach AI how to complete specific tasks in a repeatable way, whether that's creating documents with your company's brand guidelines, analyzing data using your organization's specific workflows, or automating personal tasks.

## Cross-Platform Compatibility

These skills work across multiple AI platforms:

| Platform | How to Use |
|----------|-----------|
| **Claude** (Code / .ai / API) | Plugin marketplace, upload, or API |
| **ChatGPT** | Paste into Custom Instructions or Project Instructions |
| **Kiro** | Place in `.kiro/skills/` or `.agent/skills/` |
| **GitHub Copilot** | Reference in `.github/copilot-instructions.md` |
| **Gemini** | Load via `activate_skill` or system prompt |
| **Cursor / Windsurf** | Include in rules files |
| **Any LLM API** | Include SKILL.md content in system prompt |

## About This Repository

This repository contains skills that demonstrate what's possible with AI skill systems. These skills range from creative applications (art, music, design) to technical tasks (testing web apps, MCP server generation) to enterprise workflows (communications, branding, etc.).

Each skill is self-contained in its own folder with a `SKILL.md` file containing the instructions and metadata. Browse through these skills to get inspiration for your own skills or to understand different patterns and approaches.

Many skills in this repo are open source (Apache 2.0). Document creation and editing skills in [`skills/docx`](./skills/docx), [`skills/pdf`](./skills/pdf), [`skills/pptx`](./skills/pptx), and [`skills/xlsx`](./skills/xlsx) are source-available for reference.

## Disclaimer

**These skills are provided for demonstration and educational purposes only.** The implementations and behaviors you receive may differ across platforms. These skills are meant to illustrate patterns and possibilities. Always test skills thoroughly in your own environment before relying on them for critical tasks.

## Skill Sets

- [./skills](./skills): Skill examples for Creative & Design, Development & Technical, Enterprise & Communication, and Document Skills
- [./spec](./spec): The Agent Skills specification
- [./template](./template): Skill template

## Creating a Basic Skill

Skills are simple to create — just a folder with a `SKILL.md` file containing YAML frontmatter and instructions:

```markdown
---
name: my-skill-name
description: A clear description of what this skill does and when to use it
---

# My Skill Name

[Add your instructions here that the AI will follow when this skill is active]

## Examples
- Example usage 1
- Example usage 2

## Guidelines
- Guideline 1
- Guideline 2
```

The frontmatter requires only two fields:
- `name` — A unique identifier for your skill (lowercase, hyphens for spaces)
- `description` — A complete description of what the skill does and when to use it

The markdown content below contains the instructions, examples, and guidelines that the AI will follow.
