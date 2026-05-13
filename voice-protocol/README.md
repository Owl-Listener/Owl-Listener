# voice-protocol

Brand strategists think in personality. Agents think in rules. `voice.md` bridges the gap.

---

## The problem

Mood boards and design tokens tell agents what something should look like. Nothing tells them what it should sound like. Brand voice guidelines exist — but they live in PDFs no agent reads, written in language too impressionistic to act on.

The result: AI-generated copy that is structurally correct and tonally wrong.

`voice.md` is a plain markdown file you place at the root of a project. It gives any AI agent a reliable, parseable specification of how your brand writes — not just what it values, but how those values show up in sentences.

---

## How it works

1. Copy `voice.example.md` and rename it `voice.md`
2. Fill in each section for your brand
3. Reference it in your agent context, system prompt, or workflow

No tooling required. Works with any LLM, any coding agent, any writing tool.

---

## The format

`voice.md` has five sections:

| Section | What it captures |
|---|---|
| `## Personality` | What this brand sounds like at its core — 3 to 5 descriptors, each with a clarifying contrast |
| `## Tonal range` | How voice shifts by context — same brand, different register |
| `## Mechanics` | Specific, enforceable writing rules |
| `## Vocabulary` | Words to use, words to avoid, brand-specific terms |
| `## Reference` | One example of the voice done right, one done wrong |

---

## Design principles

**Contrasts over adjectives.** "Warm" means nothing to an agent. "Warm but never gushing" is a constraint it can apply.

**Context-aware tone.** A brand that sounds the same in an error message as in a campaign headline hasn't been thought through. The tonal range section forces that thinking.

**Enforceable mechanics.** Personality is hard to evaluate. Rules are not. voice.md separates the two.

**One file, no dependencies.** Place it anywhere, reference it anywhere. No schema validation, no build step, no tooling required.

---

## Relationship to mood.md

`mood.md` captures the visual and atmospheric feel of a brand — the images it calls to mind, the textures and light it evokes.

`voice.md` captures the verbal identity — how that same brand writes.

They are complementary. Use both when you want an agent to work within a complete brand context.

---

## See also

→ [mood-protocol](https://github.com/Owl-Listener/mood-protocol) — the visual/atmospheric equivalent  
→ [voice.example.md](./voice.example.md) — a filled-in example  
→ [Owl-Listener](https://github.com/Owl-Listener/Owl-Listener) — the broader design × AI toolkit
