# AI Skills Pack

Reusable AI skills for development, design, analysis, writing, and automation — compatible across multiple AI platforms.

## Supported Platforms

| Platform | Skill Format | How to Load |
|----------|-------------|-------------|
| **Claude** (Code / .ai / API) | `SKILL.md` in folders | Plugin marketplace, manual upload, or API |
| **ChatGPT** (Custom GPTs / Projects) | Copy `SKILL.md` content | Paste into Custom Instructions or Project Instructions |
| **Kiro** | `SKILL.md` in `.kiro/skills/` or `.agent/skills/` | Auto-discovered from workspace |
| **GitHub Copilot** | `SKILL.md` or `.github/copilot-instructions.md` | Place in repo, reference in prompts |
| **Gemini** (CLI / API) | `SKILL.md` content | Load via `activate_skill` or paste into system prompt |
| **Cursor / Windsurf** | `SKILL.md` or rules files | Place in `.cursorrules` / project rules |
| **Any LLM API** | Raw markdown | Include in system prompt or context |

## Skill Categories

### Personal (Writing & Thinking)
| Skill | Description |
|-------|-------------|
| `clear-concise-writing` | Rewrite content for clarity and brevity |
| `writing` | Versatile professional writing assistant |
| `simplify` | Make complex information plain and clear |
| `research` | Find, summarize, and extract useful info |
| `problem-solving` | Break down and solve complex problems step-by-step |

### Build (Development)
| Skill | Description |
|-------|-------------|
| `creator` | Turn ideas into working solutions quickly |
| `frontend` | Create clean, modern UI interfaces |
| `testing` | Find and fix code issues |
| `ui-ux` | Senior UI/UX design and product strategy |
| `performance-optimization` | Make apps faster and more efficient |
| `vercel-agent` | Vercel deployment and frontend delivery |
| `web-design-guidelines` | Review UI against web interface best practices |

### System (Advanced / Specialized)
| Skill | Description |
|-------|-------------|
| `frontend-design` | Production-grade, distinctive frontend interfaces |
| `brand-guidelines` | Apply brand colors and typography consistently |
| `algorithmic-art` | Generative art with p5.js and seeded randomness |
| `mcp-builder` | Build MCP servers for LLM-service integration |
| `skill-creator` | Create, test, and improve AI skills |
| `web-artifacts-builder` | Multi-component web artifacts (React/Tailwind/shadcn) |
| `internal-comms` | Internal communications (updates, newsletters, FAQs) |
| `canvas-design` | Canvas-based visual design |
| `doc-coauthoring` | Collaborative document writing |
| `theme-factory` | Generate design system themes |

### Design (Taste Skills)
| Skill | Description |
|-------|-------------|
| `taste-skill` | High-agency frontend with anti-AI-slop design rules |
| `brutalist-skill` | Industrial brutalism and tactical telemetry UI |
| `gpt-tasteskill` | Awwwards-level design with GSAP motion |
| `minimalist-skill` | Refined minimalist interfaces |
| `soft-skill` | Soft, approachable UI aesthetics |
| `redesign-skill` | Redesign existing interfaces |

## How to Use

### Quick Start (Any Platform)

1. Pick a skill from the categories above
2. Find its `SKILL.md` file in the corresponding folder
3. Load it into your AI platform:
   - **System prompt**: Copy the SKILL.md content into your system/custom instructions
   - **Context file**: Reference the file in your project workspace
   - **API call**: Include the content in your messages array

### Platform-Specific Setup

See [CROSS-PLATFORM-GUIDE.md](CROSS-PLATFORM-GUIDE.md) for detailed instructions per platform.

## Skill Format

Every skill follows the same structure:

```
skill-name/
├── SKILL.md          # Required — instructions and metadata
├── templates/        # Optional — starter files
├── scripts/          # Optional — automation scripts
├── references/       # Optional — documentation
└── assets/           # Optional — fonts, images, resources
```

The `SKILL.md` file uses YAML frontmatter for metadata and markdown for instructions:

```markdown
---
name: my-skill
description: What this skill does and when to use it
---

# Skill Name

[Instructions the AI follows when this skill is active]
```

## Contributing

Each skill is self-contained. To add a new skill:

1. Create a folder with a descriptive name
2. Add a `SKILL.md` with frontmatter (`name`, `description`) and instructions
3. Keep instructions clear, actionable, and platform-agnostic
4. Test across at least two platforms before submitting

## License

Skills in this pack use mixed licensing. Check individual `LICENSE.txt` files within each skill folder. Most example skills are Apache 2.0.
