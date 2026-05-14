# tokens-protocol

Agents can read your token values. They can't read your intent. `tokens.md` fills the gap.

---

## The problem

Design tokens exist in most mature projects — as Figma variables, CSS custom properties, Tailwind configs, or style-dictionary outputs. The values are there. What's missing is the layer above the values: the semantic intent, the usage rules, the constraints that tell an agent *why* a token exists and *when* to reach for it.

The result: AI-generated UI that uses the right design system but makes the wrong choices. Correct hex, wrong context. Valid spacing value, wrong scale level. Functional — but off.

`tokens.md` annotates your existing token system with the intent agents are missing. It doesn't replace your tokens. It makes them readable.

---

## How it works

1. Copy `tokens.example.md` and rename it `tokens.md`
2. Fill in each section — values, semantic roles, usage rules
3. Add a `## Source` section pointing to where your actual token values live
4. Reference it in your agent context, system prompt, or workflow

No tooling required. Works alongside any token format: Figma variables, CSS custom properties, Tailwind, style-dictionary, or plain JSON.

---

## The format

`tokens.md` has seven sections:

| Section | What it captures |
|---|---|
| `## Color` | Semantic roles with values and usage rules |
| `## Typography` | Type scale with semantic labels and context |
| `## Spacing` | Scale with intent — component, layout, page |
| `## Elevation` | Shadow levels and what they signal |
| `## Motion` | Duration and easing with usage context |
| `## Radius` | Border radius scale with component guidance |
| `## Source` | Where your actual token values live |

---

## Design principles

**Intent over values.** An agent can import your Tailwind config. What it can't import is the decision that `red-600` means destructive and `red-400` means warning. Capture the decisions, not just the values.

**Semantic over primitive.** Name tokens by role, not by appearance. `color.surface.danger` tells an agent more than `#fee2e2`. Where you have both, map primitive to semantic.

**Usage rules, not just definitions.** Every token entry includes what it's for *and* what it's not for. The second part is often more useful.

**Thin by design.** `tokens.md` points to your source of truth — it doesn't duplicate it. Keep it short enough to paste into a context window.

---

## Relationship to mood.md and voice.md

`mood.md` captures the atmospheric and visual feel of a brand.  
`voice.md` captures the verbal identity — how the brand writes.  
`tokens.md` captures the systematic visual grammar — the specific values and rules that implement the brand in UI.

Use all three when you want an agent to work within a complete brand context.

---

## Relationship to agent-ready

[agent-ready](https://github.com/Owl-Listener/agent-ready) scores how AI-readable your Figma file is — naming conventions, structure, accessibility. It's a diagnostic you run once and fix.

`tokens.md` is a runtime context file you give an agent every time you ask it to generate UI. It's not checking anything — it's specifying intent. The two are complementary: agent-ready makes your Figma file readable, tokens.md tells the agent what the tokens in that file actually mean.

tokens-protocol is also format-agnostic. agent-ready is Figma-specific. tokens.md works whether your tokens live in Figma variables, Tailwind, CSS custom properties, or JSON.

---

## See also

→ [mood-protocol](https://github.com/Owl-Listener/mood-protocol) — atmospheric and visual intent  
→ [voice-protocol](https://github.com/Owl-Listener/voice-protocol) — verbal identity  
→ [agent-ready](https://github.com/Owl-Listener/agent-ready) — Figma file readiness diagnostic  
→ [tokens.example.md](./tokens.example.md) — a filled-in example  
→ [Owl-Listener](https://github.com/Owl-Listener/Owl-Listener) — the broader design × AI toolkit
