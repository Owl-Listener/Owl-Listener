# Felt Labs — Strategy Memo

## Context

MC Dean (Owl-Listener) is contemplating a startup, **Felt Labs**, and asked for (a) a read on
the existing collection and (b) a purpose, direction, and product fit. The conversation
established hard constraints that rule out several "obvious" plays:

- **It has to sell itself.** The founder is not a salesperson and believes great products are
  naturally in demand. This eliminates sales-led motions (evals, benchmarks, enterprise
  observability) as the *wedge* — they require evangelism and long cycles.
- **Fast PMF, customers ASAP.** Bottoms-up, self-serve, individual-as-buyer.
- **Always experience × design × AI.** The brand's permanent territory.
- **Primary customer: AI product builders.**

This memo is the written direction, positioning, and roadmap.

## The read on the existing collection

`Owl-Listener` is not software — it's an index pointing at ~11 sibling repos. Read together
they form one coherent body of work around a single unclaimed idea, stated in the README's own
closing line: *"the discipline of designing the relationship between a human and a new kind of
intelligence."* The collection breaks into layers:

- **Intent formats** — `mood-protocol`, `voice-protocol`, `tokens-protocol`,
  `perceptual-protocols` (a proto-standard; the most ownable thing).
- **A tool** — `agent-ready` (Figma plugin + `checks.js`; the only product-shaped artifact).
- **Knowledge/authority** — `agent-design-primer` (30k words on trust, refusals, plan
  visibility, accessibility), `ai-design-field-guide`.
- **Distribution** — `designer-skills`, `ai-design-skills`, `inclusive-design-skills`,
  `designpowers`.
- **Credibility** — `REFERENCES.md`, `RESEARCH.md` (research-to-practice rigor; rare).

**Special note on `ai-design-skills`** (44 skills / 18 commands / 6 plugins for Claude Code +
Gemini: model-interaction design, alignment reasoning, system-behavior shaping, evaluation,
orchestration, prompt architecture). This is the **research-grounded knowledge backbone** — it
encodes *which* trust/interaction patterns matter and *why* (HCI papers → practice via
RESEARCH.md). It is the "why" behind every Felt UI component, and it enables a defensible loop
competitors can't copy (see "The skills → components loop" below).

**Verdict:** a strong, research-grounded *point of view* and *proof of credibility* — but a
constellation, not a product. Nothing a stranger can adopt and return to tomorrow. The
collection is Felt Labs' moat (taxonomy + taste + inclusivity), not its product. We are NOT
repackaging this; it becomes the credibility engine behind a new build.

## Purpose & positioning

**Felt Labs builds the human-experience layer for AI products — starting by *shipping* it, not
measuring it.**

**Product: Felt UI** — an open-source, design-led, **inclusive-by-default React component kit
for AI/agentic interfaces.** The "trust primitives" of an AI product, done with craft and
accessibility, available in minutes.

Positioning line: **"shadcn for AI products."** The kit that makes an AI product *feel*
trustworthy and crafted out of the box.

## Standing principle: augment, don't replace

Every Felt surface amplifies the practitioner (designer / content designer / engineer); none
aims to replace them. In order of force: (1) **Go-to-market** — "replace the human" sells
top-down to managers cutting headcount (the hard, sales-led motion to avoid); "amplify the
human" sells bottoms-up to the practitioner-as-buyer (sells itself). (2) **Evangelists** —
threatening designers turns Felt's most natural champions into resisters. (3) **Substance** —
automate the *toil* (boilerplate, consistency, a11y checks, keeping specs in sync across
handoffs), never the *judgment* (taste, edge cases, refusal ethics, knowing the user), which
is where models are weakest and Felt's research backbone is strongest. (4) **Brand** — a
replace-the-designer product contradicts Owl-Listener's ethos (inclusive by default; designing
the human–AI *relationship*), which is the moat. Net: replace the handoff, not the human.

## Why this satisfies every constraint

- **Sells itself.** Component libraries are the strongest organic, no-salesperson demand in
  software: shadcn/ui (zero sales → industry default), Tailwind UI/Catalyst (tiny team,
  multi-million revenue, no sales force), Vercel AI SDK / AI Elements (proves AI-UI demand is
  hot *now*). Devs find them, `npm install`, and tell other devs. The artifact is the
  marketing.
- **Fast PMF.** 5–8 beautiful, genuinely useful components shippable in ~2 weeks; adoption
  same-day; time-to-value in minutes; the individual builder is both user and buyer.
- **Experience × design × AI, permanently.** It is literally the collection turned into
  running code people want.

## Unfair advantage (the wedge competitors can't copy)

Existing AI-UI kits are **engineer-built and functional** (generic gray chat boxes). None are
**design-led, experience-first, and inclusive-by-default.** That gap is exactly the founder — a
designer with real agentic-UX research, in a room full of engineers. Felt's durable niche:
**the AI product kit that actually feels good and includes everyone.** Each primitive is the
collection made tangible:

- `agent-design-primer` trust calibration → `<Confidence>` / uncertainty primitive
- plan visibility → `<Plan>` / `<Steps>` (agent plan surface) — signature
- graceful refusals → decline/limit patterns
- `inclusive-design-skills` → accessibility baked into every primitive (keyboard, SR-friendly
  streaming via ARIA live regions, reduced-motion) — genuinely hard, under-served
- `voice-protocol` / `mood-protocol` → themeable tone & feel

## The skills → components loop (the moat)

`ai-design-skills` already encodes the research-backed patterns for AI-product UX as Claude
Code / Gemini plugins. Felt UI turns those same patterns into shippable, accessible code. That
pairing creates a loop no engineer-built kit can replicate:

> **Skills know the patterns (the agent) → Felt UI ships the patterns (the code).** A builder
> invokes a skill in Claude Code; it scaffolds the matching Felt component — already
> accessible, already research-grounded, already on-brand via voice/mood protocols.

Competitors can copy a component's *look*; they can't copy the research-to-component pipeline
behind it. This is the durable differentiation. Practically: each MVP primitive should map to
an existing skill, and a `felt` Claude Code skill/command should be able to drop the component
into a project.

## Critical strategic call: build *on* the ecosystem, not against it

Ship Felt as a **shadcn-registry-compatible set of components built on Radix + Tailwind**, not
a competing framework. Benefits: instant distribution (the shadcn audience *is* AI builders),
near-zero "why switch" friction, inherited accessibility primitives from Radix to extend, and
`npx`-style install. This is the single biggest accelerant to PMF. **Do not rebuild shadcn —
extend it with the AI-specific trust primitives nobody else has.**

## MVP scope (the wedge — the 6 "trust primitives")

Lead with the components no other kit does well, not generic buttons:

1. **`<Plan>` / `<Steps>`** — agent plan visibility, live status per step.
2. **`<ToolCall>` / action card** — show what the agent is doing, with approve/deny.
3. **`<Confidence>`** — calibrated uncertainty / "how sure am I" affordance.
4. **`<Citation>` / source attribution** — trustworthy grounding.
5. **`<Refusal>` / decline state** — graceful limits, not dead ends.
6. **Accessible streaming `<Message>` + `<Composer>`** — first-class streaming, stop/regen,
   attachments, and SR-accessible live updates (the hard, differentiating part).

Every primitive: accessible by default, themeable, copy-paste, beautifully crafted.

### Example: `<ToolCall>` in an engineer's hands

The primary user is **the engineer who is not a designer**, shipping an AI feature. They have
an agent that can take real actions (look up orders, issue refunds, edit records); it works,
but the UI is a gray chat box, users don't trust it, and support tickets pile up. One line —
`npx felt add tool-call` — and they wrap the agent's actions:

```tsx
<ToolCall
  name="Issue refund"
  args={{ order: "#48213", amount: "$129.00", customer: "j.lee@…" }}
  reversible={false}        // Felt flags destructive, hard-to-undo actions
  status={status}           // "proposed" | "running" | "done" | "failed"
  onApprove={runRefund}
  onDeny={cancel}
/>
```

What renders is a calm, on-brand action card (not a wall of JSON) that shows intent and
parameters *before* acting, surfaces a "can't be undone" warning, exposes honest status
including a graceful failed state, is keyboard- and screen-reader-accessible by default, and
themes to the app's brand. The engineer gets the research-backed UX they didn't know to build.

## Go-to-market (distribution = the product)

- A **gorgeous docs site** with live, copy-paste components is the marketing.
- One **flagship open-source demo** built entirely from Felt (a complete agent console or AI
  chat app) engineered to go viral on its own.
- Seed through existing channels: the *Marie Claire Dean* Substack, the Owl-Listener audience,
  `designer-skills` users, X/Bluesky, Product Hunt, the shadcn registry ecosystem.
- Lean hard on the **inclusive-by-default** story as both differentiator and PR angle: "the
  first accessible AI component kit."

## Monetization (open core — no salesperson required)

- **Felt UI** — free, MIT (the ethos + the funnel) → viral adoption.
- **Felt Pro** — premium blocks, full **templates/starters** ("a beautiful agent console," "a
  trustworthy AI chat app"), and themes. One-time license + subscription for updates (the
  Tailwind UI model: significant revenue, zero outbound sales).
- Later: themes marketplace, sponsorships.

## Roadmap

- **Phase 0 (wk 0–2):** ship the 6 trust primitives + docs site + 1 flagship demo as a
  shadcn-compatible registry. Launch.
- **Phase 1 (wk 2–8):** install CLI (`npx felt add ...`), more components, theming wired to
  voice/mood protocols, first Pro template. Build the audience loop.
- **Phase 2 (mo 3–6):** launch **Felt Pro** (templates/blocks); mirror a **Figma kit** of the
  primitives; design-to-code.
- **Phase 3 (mo 6–12):** two differentiated expansions, both earned by component adoption:
  - **Felt Studio** — the behavior/voice-DESIGN layer (see "Adjacent bet" below), integrating
    with prompt registries rather than competing on prompt management.
  - **Felt Index** — the experience benchmark/evals as **authority + data flywheel**, the
    correct year-two home for the original eval/research idea (never the year-one wedge).

## Adjacent bet considered and deliberately deferred: the behavior layer ("Felt Studio")

The founder has personally watched the **content-designer → engineer prompt handoff** break at
work (prompts authored in docs, thrown over the wall, intent lost, no versioning/testing). That
is a real, firsthand pain and a tempting wedge. We deferred it for clear reasons:

- The obvious form of it (author + version + evaluate prompts, no-code editor for non-eng) is
  **already owned by PromptLayer** (cake logo) and a crowded field — Langfuse, Humanloop,
  Vellum, PromptHub, Latitude, Agenta, plus lab consoles. Red ocean.
- It is bought as **ops/infra** (eval + procurement) — the evangelism-heavy, sales-led motion
  the founder explicitly cannot/does not want to run.
- The only genuinely open gap is **conversation/voice DESIGN as a craft** (voice, persona,
  tone, refusal behavior, edge-case language, a11y of wording) — a design discipline, not a
  prompt-string registry. That is narrower and less proven, and adding versioning/eval drags it
  back into PromptLayer's ring.

**Decision:** Felt UI (components) is the wedge — uncontested, self-serve, sells itself. The
behavior layer returns later as **Felt Studio**, positioned as the *design-craft* layer that
**integrates with / exports to** prompt registries (e.g. PromptLayer), not a rebuild of them.
This keeps Felt on the design side of every line, where it is unbeatable.

## Risks & mitigations

- **Vercel/others move into design-led territory** → move fast, own the inclusive +
  trust-craft niche and the design-taste brand they structurally aren't.
- **Component-kit commoditization** → differentiate on AI-specific trust primitives + a11y +
  taste; build on shadcn rather than competing on generic components.
- **OSS maintenance burden / solo bandwidth** → keep the free core tight; monetize templates;
  build with AI coding agents (the founder's core skillset). Stay lean.
- **"Nice-to-have" perception** → tie components to outcomes builders feel (trust, fewer
  support tickets, accessibility compliance) in docs and demos.

## Next steps

1. Validate the wedge: pick the single most painful primitive (`<ToolCall>` or `<Plan>`) and
   build it beautifully, accessible, shadcn-compatible.
2. Stand up a docs site with a live, copy-paste demo of that one component.
3. Build the flagship demo app around it and post it through existing channels.
4. Map each primitive to its `ai-design-skills` skill, and prototype the `felt` Claude Code
   command that scaffolds a component into a project (the moat loop).
