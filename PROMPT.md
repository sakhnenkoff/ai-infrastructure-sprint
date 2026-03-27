Read CLAUDE.md first for full project context.

This is an AI Infrastructure Sprint — a 30-minute interactive web experience that teaches senior engineers how to build AI infrastructure (CLAUDE.md, rules, docs, skills, integrations).

The sprint and carousel have been redesigned with confrontational, research-grounded copy. The UX has a progressive architecture diagram and terminal companion model. All merged and pushed to main.

## What needs work

1. **Content depth in block narratives** — Each block has a `narrative` field in the BLOCKS JS object (index.html). These are the insight paragraphs that appear in the `.block-narrative` zone. They need to be richer — more specific examples, more "here's what the best teams actually do" energy. The research briefing at `docs/superpowers/specs/research-briefing.md` has data we haven't fully used. You can also query the NotebookLM notebook (ID: f36585d1-4156-49db-bcb3-eda7143944cf) with `notebooklm ask "..."` for specific questions.

2. **Copy polish pass** — Read through the entire sprint flow (hook → diagnosis → blocks 1-5 → completion) and flag anything that feels weak, inconsistent, or thin. Fix it. The voice should be consistent: confrontational, second-person, data-backed, "the engineer replacing you does X."

3. **README update** — Still says "7 guided blocks." Needs to match the current 5-block structure and new positioning.

4. **Overall vibe check** — Open index.html locally and click through the whole experience. Does it feel like something a senior engineer would actually want to complete? Or does it still feel like a checklist? If something feels off, fix it.

## What NOT to change

- Hook copy (locked)
- Diagnosis questions and scoring (locked)
- Design system (fonts, colors, components)
- Architecture diagram sidebar behavior
- State management system
- Carousel content (just aligned, don't touch)

## Key context

- Audience: senior engineers + engineering leads who already use AI tools
- Frame: "the engineer replacing you" — what top 33% do differently
- Philosophy lines to weave in: "that's not adoption, that's just access", "the tool isn't the bottleneck, the environment is", "infrastructure compounds"
- Tool-agnostic on integrations — don't evangelize MCP specifically
