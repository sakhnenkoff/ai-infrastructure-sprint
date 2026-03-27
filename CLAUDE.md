# AI Infrastructure Sprint — Project Context

**Positioning:** "AI Infrastructure for Engineers — because context is the multiplier."

**Author:** Matvii Sakhnenko

## Repo Structure

- `index.html` — Single-page HTML/CSS/JS sprint experience. Brutalist design (Space Grotesk + JetBrains Mono, black/white, off-white blocks). 5 blocks + diagnosis + completion.
- `carousel/index.html` — LinkedIn carousel (10 slides, Quiet Light theme). Visual brand reference.
- `assets/` — Screenshots for README.
- `docs/superpowers/specs/` — Design specs (gitignored, local only).
- `docs/superpowers/plans/` — Implementation plans (gitignored, local only).

## Current State (2026-03-27)

The sprint was redesigned from a 7-block beginner tutorial to a 5-block confrontational experience for senior engineers. Content redesign is done. Two open problems remain:

1. **Content depth** — copy needs to be grounded in real research, not generic claims. A NotebookLM "Source of Truth" notebook exists with 50+ sources on context engineering, AI productivity data, team adoption patterns.
2. **UI/UX engagement** — the experience is still passive checkbox ticking. Needs progressive reveal (architecture diagram fills as you complete blocks) and terminal-companion model (narrative on web, actions in terminal).

## Sprint Structure

- **Hook:** "the gap between you and the engineer replacing you isn't talent. it's 6 files in a .claude/ directory."
- **Diagnosis:** 3 questions, 6-point scale, gap-based reveal
- **Block 1:** Context layer — CLAUDE.md, .claude/rules/, .claude/docs/
- **Block 2:** Skill layer — encode a real team workflow
- **Block 3:** Orchestration — Plan Mode + subagents on a real task
- **Block 4:** Integrations — MCP servers (Figma, Atlassian, Context7, Playwright, XcodeBuildMCP)
- **Block 5:** The system — architecture reveal, compound test, maintenance rules
- **Completion:** "next time someone asks what changed — you have an answer."

## Architecture Pattern (taught by the sprint)

```
CLAUDE.md (project context — architecture, conventions, key files)
  └→ .claude/
      ├→ rules/ (always-loaded corrections)
      ├→ docs/ (reference material on demand)
      ├→ skills/ (encoded workflows, invokable by name)
      └→ MCP servers (external tool access)
```

## Design System

- **Fonts:** Space Grotesk (display), JetBrains Mono (code/mono)
- **Colors:** Black (#000), white (#fff), off-white (#f5f5f0), grey (#999), green (#4ade80 for code)
- **Components:** .tag (black box label), .btn/.btn-ghost, .codeblock (black bg, green text), .step (checkbox + text), .proof (thick border-top section)
- **Layout:** Center-aligned, max-width 720-800px, min-height 100vh per screen

## Content Principles

- **Second person only** — "you", never "they" or "the engineer"
- **Every step is an action** — "Run this" not "Consider doing this"
- **Opinionated** — "Do this" not "You could consider"
- **Confrontational** — each block opens with a spicy observation
- **Technical respect** — audience already uses AI tools, never explain basics
- **No emojis**

## Related Repos

- **Full course:** `github.com/sakhnenkoff/ai-infrastructure-course`
- **FINN iOS workshop** (internal): `github.schibsted.io/matvii-sakhnenko/ios-ai-workshop` — 2-day hands-on for Vend iOS team
- **LinkedIn carousel skill:** `github.com/sakhnenkoff/linkedin-carousel`

## Research

- **NotebookLM notebook:** "AI Infrastructure for Engineers — Source of Truth" (ID: f36585d1-4156-49db-bcb3-eda7143944cf) — 50+ sources on context engineering, AI productivity data, CLAUDE.md patterns, MCP best practices, team adoption
