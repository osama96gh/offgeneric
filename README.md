# OffGeneric

**Make AI output original instead of generic, while keeping it recognizable.**

AI models converge on the same answers: the same names, the same purple-gradient login page, the same ideas. Asking for "more creative" barely helps. OffGeneric is an agent skill that pulls real seed material from outside sources on the web, mixes it into your request, and checks that the result still makes sense to a fresh reader.

## Install

**Any coding agent** (Claude Code, Codex, Cursor, Gemini CLI and many more):

```bash
npx skills add osama96gh/offgeneric
```

**Manual install**

| Tool | Steps |
|---|---|
| Claude Code | Copy `skills/offgeneric` to `~/.claude/skills/offgeneric` |
| Codex | Copy `skills/offgeneric` to `.agents/skills/offgeneric` in your project (check the Codex docs for the current path) |
| claude.ai / Claude app | Download `offgeneric.zip` from [Releases](../../releases) and upload it under Skills |
| OpenAI API | Upload the `skills/offgeneric` folder or the zip as a skill |
| ChatGPT / any other chat AI | Paste the contents of [`SKILL.md`](skills/offgeneric/SKILL.md) into your custom instructions or project instructions |

## Use

Just ask for something creative. The skill triggers on its own:

> Suggest 5 names for my app that monitors support chats and alerts on spikes.

> Design a login page for a meditation app as a single HTML file.

Works for names, slogans, titles, UI and visual style, logos, palettes, product ideas, stories and content angles. Not for facts, math or debugging.

## How it works

1. **Anchor**: decide what must stay recognizable (the meaning of a name, the conventions of a login page).
2. **Anti-seeds**: write down the generic answers, so nothing delivered looks like them.
3. **Seeds**: pull raw material from three outside sources: one adjacent field, one far field, a little randomness.
4. **Blend**: anchor + twist. The seed changes the result; it never replaces the meaning.
5. **Five-second test**: a reader with no context guesses what each result is. Wrong guesses are dropped.
6. **Present**: a short list, each result with its seed and source.

The rule above all: **off-generic in style, never in meaning or function.**

## Before / after

<!-- Add your comparison screenshots here -->

## Requirements

The agent needs **web access** to pull seeds. Without it, the skill falls back to the model's memory, which is exactly the generic behavior it tries to avoid.

## License

[MIT](LICENSE)
