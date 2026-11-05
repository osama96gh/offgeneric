---
name: offgeneric
description: Makes creative output original instead of generic, while keeping it recognizable. Use whenever the user asks for something open-ended where the typical AI answer is the problem — naming a product, company, feature or skill; slogans, taglines, titles; designing a page, UI, logo, palette or visual style; product, feature, story or content ideas. Pulls real seed material from outside sources on the web instead of relying on the model's memory. Not for factual questions, math, debugging or anything with one correct answer.
---

# OffGeneric

Language models converge on the same answers. Asking for "more creative" barely helps; outside material does. This skill pulls real seeds from the web, mixes them into the request, and checks the result is still understandable.

**One rule above all: be off-generic in style, never in meaning or function.** A name must still say what the thing does. A login page must still look like a login page.

## The flow

Follow these steps in order. Keep it fast: 3 sources, 10–20 candidates, deliver the best few.

### 1. Anchor — what must stay recognizable
Write down, in plain words:
- **Purpose:** what the result is for and who sees it.
- **Anchor words or conventions:** the plain vocabulary of the problem (for names) or the conventions people rely on (for UI: fields, buttons, layout cues).
- **Check the anchor for ambiguity in the audience's world.** Example: "seed" reads as seed data or crypto to developers. Prefer anchors that describe the *problem solved* or the *outcome*.

### 2. Anti-seeds — the generic answers to avoid
- Write your own default answer first, quickly. That is the anti-seed.
- Add what already exists: a quick web search for existing products/names in the space, or for visuals the usual AI look (centered card on a soft gradient, purple accent, one default font, glassmorphism, emoji icons).
- Nothing you deliver may resemble an anti-seed.

### 3. Seeds — real material from outside
- Pick **3 sources** whose material suits the output (words for names, artworks or design movements for visuals, other industries or nature for ideas):
  - **Adjacent** (a related field) — most results should come from here.
  - **Far** (an unrelated field, used as analogy) — a few results.
  - **Random** — a little spice only.
- **Harvest raw material, not summaries.** Pull the actual lists, terms, colors or items from the page yourself. Don't let a summarizer pick the "interesting" ones, and never invent seeds from memory.
- Keep the source of each seed so it can be cited.

### 4. Blend — anchor + twist
- Every candidate = **anchor** (carries the meaning) + **twist** (from a seed).
- The seed changes the anchor; it never replaces it. A bare seed word as a name is a failure, however pretty.
- For visuals, put the twist in style: palette, type, composition, texture, motion, copy tone. Keep the anchor conventions intact.

### 5. Five-second test — fresh eyes
- Show the candidates to a reader with **no context** and ask for a first guess of what each is.
  - If you can start a subagent, use one with no context and a cheap model. Give it only the bare candidates (names list, or the HTML file / a screenshot for visuals).
  - Names: "Guess what each does in 10 words."
  - Visuals: "What page is this? What would you click first?"
  - If no subagent is available, do a cold read yourself: judge each candidate as someone who has seen only it.
- Drop anything guessed wrong. If most fail, the anchor is wrong — fix it and redo step 4, not just step 3.

### 6. Present
Short and scannable. For each result: the result, its **seed** and **source**, and one line on why it fits. For visuals, deliver the artifact plus a 2–3 line note of the seeds behind it. Deliver what the user asked for (e.g. 5 names) — not more.

## Notes
- Default ratio: about 60% adjacent, 30% far, 10% random.
- If the user names a constraint (length, tone, domain, brand), it becomes part of the anchor.
- If availability matters (names, domains), offer a quick check at the end; don't skip the creative steps to do it.
