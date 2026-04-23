# Cross-Platform Compatibility Guide

This guide explains how to use skills from this pack across different AI platforms.

## How Skills Work

A skill is a set of instructions (in `SKILL.md`) that teaches an AI assistant how to perform a specific task. The instructions are written in plain markdown, making them portable across any platform that accepts text-based prompts or system instructions.

## Platform Setup

### Claude (Anthropic)

**Claude Code (CLI)**
```bash
# Register as a plugin marketplace
/plugin marketplace add <path-to-skills>

# Install a skill set
/plugin install example-skills@anthropic-agent-skills
```

**Claude.ai**
- Go to Settings > Skills
- Upload the `SKILL.md` file or the entire skill folder
- The skill activates automatically when relevant

**Claude API**
- Include the SKILL.md content in your system prompt or use the Skills API

### ChatGPT (OpenAI)

**Custom GPTs**
1. Go to "Create a GPT" or edit an existing one
2. In the "Instructions" field, paste the content of the `SKILL.md` file
3. For skills with templates/scripts, upload those as Knowledge files

**Projects**
1. Open a Project in ChatGPT
2. Add the `SKILL.md` content to the Project Instructions
3. Upload any supporting files (templates, references) to the Project

**API**
```json
{
  "model": "gpt-4o",
  "messages": [
    {
      "role": "system",
      "content": "<paste SKILL.md content here>"
    },
    {
      "role": "user",
      "content": "Your task..."
    }
  ]
}
```

### GitHub Copilot

**Copilot Chat (VS Code / CLI)**
1. Place skill folders in your repository
2. Reference them in `.github/copilot-instructions.md`:
   ```markdown
   When working on frontend tasks, follow the instructions in .agent/skills/build/frontend/SKILL.md
   ```
3. Or mention skills directly in chat: "Use the frontend skill to build this component"

**Copilot Workspace**
- Skills in the repo are auto-discovered when referenced

### Google Gemini

**Gemini CLI**
- Skills activate via the `activate_skill` tool
- Place skill folders in your project and reference them in `GEMINI.md`

**Gemini API**
```json
{
  "system_instruction": {
    "parts": [{"text": "<paste SKILL.md content here>"}]
  }
}
```

### Cursor

1. Create a `.cursorrules` file in your project root
2. Paste the SKILL.md content, or reference it:
   ```
   Follow the instructions in .agent/skills/build/frontend/SKILL.md for all UI work.
   ```
3. For multiple skills, combine them in `.cursor/rules/` directory

### Windsurf

1. Add skill content to `.windsurfrules` in your project root
2. Or place skills in the project and reference them in prompts

### Kiro

1. Place skill folders in `.kiro/skills/` or `.agent/skills/`
2. Skills are auto-discovered from the workspace
3. Reference skills in steering files at `.kiro/steering/`

### Any LLM API (Generic)

Include the SKILL.md content in your system prompt or as a context message:

```python
# Python example with any OpenAI-compatible API
with open("path/to/SKILL.md") as f:
    skill_content = f.read()

response = client.chat.completions.create(
    model="your-model",
    messages=[
        {"role": "system", "content": skill_content},
        {"role": "user", "content": "Your task here"}
    ]
)
```

## Adapting Skills for Your Platform

### Tool References

Some skills reference platform-specific tools. Here's how to translate them:

| Skill Reference | Claude | ChatGPT | Copilot | Gemini | Generic |
|----------------|--------|---------|---------|--------|---------|
| "Read file" | `Read` tool | Code Interpreter | `@workspace` | `activate_skill` | "Read the file at..." |
| "Create file" | `create_file` | Code Interpreter | File creation | File creation | "Create a file..." |
| "Search web" | `WebFetch` | Browse | `@web` | Google Search | "Search for..." |
| "Run script" | `Bash` tool | Code Interpreter | Terminal | Shell | "Execute..." |

When a skill says "use the X tool", translate to your platform's equivalent. The intent matters more than the specific tool name.

### Subagent / Multi-step Patterns

Some advanced skills (like `skill-creator`) reference "subagents" for parallel execution. On platforms without subagent support:
- Run steps sequentially instead of in parallel
- Skip benchmark/comparison steps that require independent evaluation
- Focus on the core workflow (draft → test → review → improve)

### File System Access

Skills that reference file paths (like `templates/viewer.html`) assume the skill folder is accessible. If your platform doesn't have file system access:
- Include template content directly in the instructions
- Upload templates as knowledge/context files
- Inline any referenced content

## Tips for Best Results

1. **Start with the SKILL.md content** — it's the core of every skill
2. **Include supporting files** when the skill references them (templates, examples)
3. **Test with a simple prompt first** to verify the skill loaded correctly
4. **Combine skills** by including multiple SKILL.md contents in your system prompt
5. **Customize freely** — skills are starting points, adapt them to your needs
