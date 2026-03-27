Read CLAUDE.md first. Then read docs/superpowers/specs/research-briefing.md — that's your source of truth for data points.

## The mission

This sprint looks built but reads hollow. The structure is right, the UX works, but the content doesn't earn the reader's time yet. A senior engineer clicks through, checks some boxes, and forgets about it by tomorrow. That's the problem.

Your job: make every screen worth reading. Not by adding more — by making what's there sharper, more specific, more real. When a senior engineer finishes this sprint, they should feel like they learned something they didn't know, not just installed something they'd heard of.

## The five problems

### 1. Code snippets are fill-in-the-blank templates
Every code block says `[Describe the mistake]` or `[Your stack, key patterns]`. A senior engineer sees bracket placeholders and thinks "tutorial for beginners." Replace these with REAL examples — a realistic CLAUDE.md for a Node.js API, a realistic rule that fixes a real mistake, a realistic skill that does a real review. They can adapt real examples to their project. They can't adapt empty brackets to anything.

### 2. Data points float without sources
The sprint uses powerful stats — 91%/33% adoption gap, 69% hidden flaws, 32K token cliff, 4+ re-explanations/day. But none are cited. A skeptical senior engineer reads "69% of AI code has hidden flaws" and thinks "where'd you get that number?" The research briefing doc has the sources. Wire them in — not as footnotes, but as credibility anchors. "Research from Faros AI found..." or a small source tag.

### 3. Block narratives are uneven
Block 1 (context) and Block 3 (orchestration) have strong, specific narratives. Block 2 (skills) and Block 4 (integrations) are thinner — more descriptive than insightful. Query the NotebookLM notebook for deeper material:
```
notebooklm use f36585d1
notebooklm ask "what makes skills/encoded workflows actually work at a team level? give me specific patterns and anti-patterns"
notebooklm ask "what are the real workflow improvements teams see from integrating external tools into their AI workflow?"
```

### 4. It's still a checklist
The progressive diagram helps, but each block is still "read some text, check some boxes." The narrative should build tension WITHIN each block — start with the pain, escalate with data, then release with the action. Right now it's: opener → steps. It should feel more like: opener (pain) → narrative (why this is worse than you think) → actions (the fix) → proof (you'll know it worked).

### 5. Small fixes
- README.md still says "7 guided blocks" — update to match current 5-block structure
- Completion upsell copy ("governance policies", "moved the needle") is slightly corporate compared to the rest — match the sprint's voice
- Diagnosis question A options ("no", "nothing") are flat — they work but could have more personality

## What NOT to touch
- Hook headline and subtext — locked, they work
- Diagnosis scoring logic and tier thresholds — locked
- Architecture diagram sidebar — locked
- State management, routing, CSS — locked
- Carousel — just aligned, leave it alone
- Design system (fonts, colors, components) — locked

## Resources
- `docs/superpowers/specs/research-briefing.md` — synthesized research findings with data points
- NotebookLM notebook ID: `f36585d1-4156-49db-bcb3-eda7143944cf` — 50+ sources, query with `notebooklm ask "..."`
- `carousel/index.html` — aligned carousel for voice reference

## How to verify
Open index.html locally. Click through every screen. Read every word. Ask yourself: would a staff engineer at a top tech company find this worth their 30 minutes? If any screen makes you think "this is generic" — fix it before moving on.
