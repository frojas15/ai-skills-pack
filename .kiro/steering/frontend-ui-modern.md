---
inclusion: auto
---

# Modern Frontend UI Standards

When generating any frontend code (React, Next.js, HTML, CSS, components, pages, layouts, dashboards):

## Design Quality

Follow the anti-AI-slop design rules from #[[file:.agent/skills/system/taste-skill-main/skills/taste-skill/SKILL.md]]

Key rules always in effect:
- Never use Inter font — use Geist, Outfit, Cabinet Grotesk, or Satoshi
- Never use purple/blue AI gradients — use neutral bases with singular high-contrast accents
- Never use centered hero layouts when design variance is high — use asymmetric, split-screen, or editorial layouts
- Never use emoji in code, markup, or text content — use Phosphor or Radix icons
- Never use `h-screen` — always use `min-h-[100dvh]`
- Never use flexbox percentage math — use CSS Grid
- Never use generic 3-column card layouts — use asymmetric grids or zig-zag patterns

## Production Standards

Follow #[[file:.agent/skills/build/frontend/SKILL.md]] and #[[file:.agent/skills/system/skills-main/skills/frontend-design/SKILL.md]]

- Responsive by default (mobile-first, test at sm/md/lg/xl breakpoints)
- Accessible (proper contrast, semantic HTML, ARIA labels where needed)
- Always include loading, empty, and error states for interactive components
- Verify dependencies exist in package.json before importing any library
- Use Server Components by default in Next.js, isolate interactivity in Client Components
- Hardware-accelerate animations — only animate `transform` and `opacity`
- Use Spring physics for motion, not linear easing

## Performance

Follow #[[file:.agent/skills/build/performance-optimization/SKILL.md]]

- Lazy load heavy components and images
- Avoid unnecessary re-renders
- Keep bundle size minimal
- Use `will-change` sparingly
