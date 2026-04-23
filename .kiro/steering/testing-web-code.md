---
inclusion: auto
---

# Web Code Testing Standards

When writing, reviewing, or debugging any web code (frontend, backend, APIs, components):

## Code Quality

Follow #[[file:.agent/skills/build/testing/SKILL.md]]

- Analyze code for bugs before suggesting changes
- Check edge cases: null/undefined inputs, empty arrays, network failures, race conditions
- Verify error handling exists for all async operations
- Look for performance issues (unnecessary re-renders, memory leaks, blocking operations)

## UI Review

Follow #[[file:.agent/skills/build/ui-ux/SKILL.md]]

When reviewing or building UI:
- Check spacing consistency and visual hierarchy
- Verify responsive behavior at all breakpoints
- Ensure important actions are obvious and accessible
- Flag low contrast, confusing flows, or overloaded screens

## Web Standards

Follow #[[file:.agent/skills/build/web-design-guidelines/SKILL.md]]

- Fetch and apply the latest Web Interface Guidelines when reviewing UI code
- Output findings in `file:line` format when doing reviews
- Check accessibility, semantic HTML, and keyboard navigation

## Before Shipping Checklist

- [ ] No console errors or warnings
- [ ] Loading and error states implemented
- [ ] Responsive at mobile, tablet, and desktop
- [ ] No hardcoded secrets or API keys
- [ ] Dependencies pinned to exact versions
- [ ] Edge cases handled (empty data, long strings, slow network)
