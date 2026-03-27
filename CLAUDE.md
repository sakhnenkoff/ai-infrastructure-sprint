# AI Infrastructure Sprint — Project Context

**Positioning:** "AI Infrastructure for Engineers — because context is the multiplier."

**Author:** Matvii Sakhnenko

## Repo Structure

- `index.html` — Single-page HTML/CSS/JS sprint experience. Brutalist design (Space Grotesk + JetBrains Mono, black/white, off-white blocks). 5 blocks + diagnosis + completion. Features: progressive architecture diagram sidebar, terminal companion cues, narrative/actions zone split.
- `carousel/index.html` — LinkedIn carousel (10 slides, Quiet Light theme: IBM Plex Sans + Mono). Aligned with sprint voice and content.
- `assets/` — Screenshots for README.
- `docs/superpowers/specs/` — Design specs (gitignored, local only).
- `docs/superpowers/plans/` — Implementation plans (gitignored, local only).

## Current State (2026-03-27)

### Done
- **Content redesign** — 7-block beginner tutorial → 5-block confrontational experience for senior engineers. Research-grounded copy using data from NotebookLM (91%/33% adoption gap, 69% hidden flaws, 32K token cliff, progressive disclosure patterns).
- **UI/UX progressive reveal** — Architecture diagram sidebar fills as blocks complete. Terminal companion cues ($ prefix). Narrative/actions zone split. Block 5 compound reveal animation. State persistence.
- **Carousel alignment** — Rewritten to match sprint voice. Before/after framing on layer slides. Clear CTA directing to sprint course.
- **Content alignment** — Sprint borrows carousel's philosophy lines ("that's not adoption, that's just access", "the tool isn't the bottleneck, the environment is", "infrastructure compounds"). Carousel borrows sprint's data and edge.

### Open
- **Content depth** — Block narratives could be richer. The NotebookLM notebook has 50+ sources we've only partially mined. Each block's "narrative" field could use more specific insights, examples, and data points from the research.
- **Overall polish** — Copy pass for consistency, flow, and impact across all screens. Some blocks may still feel thin compared to the hook and completion.
- **README** — Still references "7 guided blocks" and old description. Needs update to match current sprint.

## Sprint Structure

- **Hook:** "the gap between you and the engineer replacing you isn't talent. it's 6 files in a .claude/ directory."
- **Subtext:** "next quarter someone will ask what changed since you adopted AI. what's your answer?"
- **Diagnosis:** 3 questions (CLAUDE.md status, workflow reuse, integrations), 6-point scale, gap-based reveal ("that's not adoption. that's just access.")
- **Block 1:** Context layer — CLAUDE.md audit, .claude/rules/, .claude/docs/, /context token budget
- **Block 2:** Skill layer — encode a real team workflow as a slash-command skill
- **Block 3:** Orchestration — Plan Mode on a real task + subagents
- **Block 4:** Integrations — connect one tool (Figma, Atlassian, Context7, Playwright, XcodeBuildMCP)
- **Block 5:** The system — architecture reveal, compound test, maintenance rules (wrong answer → rule, repeated workflow → skill, stale context → update)
- **Completion:** "next time someone asks what changed — you have an answer." Architecture diagram as deliverable. Course upsell.

## Architecture Pattern (taught by the sprint)

```
CLAUDE.md (project context — architecture, conventions, key files)
  └→ .claude/
      ├→ rules/ (always-loaded corrections)
      ├→ docs/ (reference material on demand)
      ├→ skills/ (encoded workflows, invokable by name)
      └→ MCP/CLI integrations (external tool access)
```

## Key UI Components

- **Architecture diagram sidebar** — Fixed right (desktop), collapsible top bar (mobile). 6 layers map to blocks. States: locked → active → completed. Driven by `updateDiagram()` + `LAYER_BLOCK_MAP`.
- **Terminal companion cues** — `$` prefix on action steps via `.step-prompt`
- **Narrative/actions split** — `.block-narrative` (insight) + `.block-actions-label` (steps)
- **Block 5 reveal** — All diagram layers animate to completed. Inline diagram (black bg, green text).
- **Sticky nav** — Bottom-right `← back` / `next →` buttons on block screens.

## Design System

- **Fonts:** Space Grotesk (display), JetBrains Mono (code/mono)
- **Colors:** Black (#000), white (#fff), off-white (#f5f5f0), grey (#999), green (#4ade80 for code)
- **Components:** .tag, .btn/.btn-ghost, .codeblock, .step, .proof, .arch-sidebar, .arch-layer, .block-narrative
- **Layout:** Center-aligned, max-width 720-800px, sidebar 260px right

## Content Principles

- **Second person only** — "you", never "they" or "the engineer"
- **"The engineer replacing you" frame** — each block shows what top performers do differently
- **Data-backed claims** — reference research (NotebookLM), never make unsourced claims
- **Before/after framing** — "without X... with X..." for layer descriptions
- **Opinionated** — "Do this" not "You could consider"
- **Technical respect** — audience already uses AI tools, never explain basics
- **Tool-agnostic integrations** — don't evangelize MCP specifically, say "connect your tools"
- **No emojis**

## Key Philosophy Lines (shared across sprint + carousel)

- "that's not adoption. that's just access."
- "the tool isn't the bottleneck. the environment is."
- "infrastructure compounds — each layer multiplies the ones below it."
- "the environment is the product."

## Related Repos

- **Full course:** `github.com/sakhnenkoff/ai-infrastructure-course`
- **FINN iOS workshop** (internal): `github.schibsted.io/matvii-sakhnenko/ios-ai-workshop`
- **LinkedIn carousel skill:** `github.com/sakhnenkoff/linkedin-carousel`

## Research

- **NotebookLM notebook:** "AI Infrastructure for Engineers — Source of Truth" (ID: f36585d1-4156-49db-bcb3-eda7143944cf) — 50+ sources on context engineering, AI productivity data, CLAUDE.md patterns, team adoption patterns, failure modes
- **Briefing doc:** `docs/superpowers/specs/research-briefing.md` — synthesized key findings
- **Key data points:** 91% adopted / 33% saw gains, 69% hidden flaws in AI code, review time up 91%, PR sizes up 154%, accuracy drops past 32K tokens, teams re-explain patterns 4+ times/day without context
