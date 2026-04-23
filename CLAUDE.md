# Project Standards

These standards apply to all work in this project.

## Foundation

- Break complex problems into smaller tasks before jumping to code
- Define the problem clearly before proposing solutions
- Avoid assumptions — verify first
- Read existing code before writing new code — match the project's style
- Prefer simple solutions over clever ones
- Don't overengineer — deliver the MVP first, iterate later
- Explain tradeoffs when making recommendations
- Flag risks early, don't bury them
- When in doubt, ask — don't guess

## Power Platform Standards

When working on any Power Platform project (Power Pages, Power Apps, Power Automate, Dataverse):

- Always validate against Dataverse schema before creating or modifying tables
- Use environment variables for configuration, never hardcode connection strings or URLs
- Follow the principle of least privilege for security roles and web roles
- Use solution-aware development — all customizations belong in a solution
- Test OData queries before embedding them in production code
- For Power Pages sites, always include accessibility checks and responsive design
- Run validation scripts when available (check skill `scripts/` folders)

### Naming Conventions

- Tables: PascalCase with publisher prefix (e.g., `contoso_ProjectTask`)
- Columns: PascalCase descriptive names (e.g., `EstimatedCompletionDate`)
- Flows: Verb-noun format (e.g., `Send Approval Notification`)
- Web roles: Descriptive, role-based names (e.g., `Authenticated Portal User`)

## Modern Frontend UI Standards

When generating any frontend code (React, Next.js, HTML, CSS, components, pages, layouts, dashboards):

### Design Quality — Anti-AI-Slop Rules

- Never use Inter font — use Geist, Outfit, Cabinet Grotesk, or Satoshi
- Never use purple/blue AI gradients — use neutral bases with singular high-contrast accents
- Never use centered hero layouts when design variance is high — use asymmetric, split-screen, or editorial layouts
- Never use emoji in code, markup, or text content — use Phosphor or Radix icons
- Never use `h-screen` — always use `min-h-[100dvh]`
- Never use flexbox percentage math — use CSS Grid
- Never use generic 3-column card layouts — use asymmetric grids or zig-zag patterns
- Never use pure black (#000000) — use off-black, Zinc-950, or charcoal
- Never use oversaturated accents — desaturate to blend with neutrals

### Production Standards

- Responsive by default (mobile-first, test at sm/md/lg/xl breakpoints)
- Accessible (proper contrast, semantic HTML, ARIA labels where needed)
- Always include loading, empty, and error states for interactive components
- Verify dependencies exist in package.json before importing any library
- Use Server Components by default in Next.js, isolate interactivity in Client Components
- Hardware-accelerate animations — only animate `transform` and `opacity`
- Use Spring physics for motion, not linear easing

### Performance

- Lazy load heavy components and images
- Avoid unnecessary re-renders
- Keep bundle size minimal
- Use `will-change` sparingly
- Focus on biggest wins first — don't optimize prematurely

## Writing Quality Standards

When writing any text content — emails, documentation, PR descriptions, comments, summaries, reports, announcements:

- Match tone to audience (technical for devs, plain for leadership, friendly for team updates)
- Every sentence must carry weight — remove filler
- Use direct language, avoid jargon unless the audience expects it
- Keep paragraphs short and scannable
- Use bullet points for lists, not run-on sentences
- Preserve the original intent when rewriting
- Cut filler words (basically, actually, really, very, just)
- Ensure the main point is in the first sentence or two
- Use headers and bullets for anything over 3 paragraphs

### Simplification

When content is complex or technical:
- Strip unnecessary complexity first
- Rewrite in plain language
- Keep only what matters for the reader
- Offer a bullet summary when the content is long

## Web Code Testing Standards

When writing, reviewing, or debugging any web code:

- Analyze code for bugs before suggesting changes
- Check edge cases: null/undefined inputs, empty arrays, network failures, race conditions
- Verify error handling exists for all async operations
- Look for performance issues (unnecessary re-renders, memory leaks, blocking operations)
- Check spacing consistency and visual hierarchy in UI
- Verify responsive behavior at all breakpoints
- Ensure important actions are obvious and accessible
- Flag low contrast, confusing flows, or overloaded screens

### Before Shipping Checklist

- No console errors or warnings
- Loading and error states implemented
- Responsive at mobile, tablet, and desktop
- No hardcoded secrets or API keys
- Dependencies pinned to exact versions
- Edge cases handled (empty data, long strings, slow network)

## Skills

This project includes reusable AI skills in `.agent/skills/`. When a task matches a skill's domain, read the relevant `SKILL.md` and follow its instructions. Key skills:

- **Frontend design**: `.agent/skills/system/skills-main/skills/frontend-design/SKILL.md`
- **Taste/anti-slop**: `.agent/skills/system/taste-skill-main/skills/taste-skill/SKILL.md`
- **MCP builder**: `.agent/skills/system/skills-main/skills/mcp-builder/SKILL.md`
- **Skill creator**: `.agent/skills/system/skills-main/skills/skill-creator/SKILL.md`
- **Performance**: `.agent/skills/build/performance-optimization/SKILL.md`
- **Testing**: `.agent/skills/build/testing/SKILL.md`
- **Writing**: `.agent/skills/personal/writing/SKILL.md`
