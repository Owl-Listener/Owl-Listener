---
description: Run a full aesthetic critique of a screen or design — hierarchy, composition, typography, and brand consistency.
argument-hint: "[screen name or description]"
---
# /critique-screen

Run a full aesthetic critique of a screen or design.

## Steps

1. **Brand context** — Check for mood.md, voice.md, and tokens.md in the project root. Note which are present.
2. **Visual hierarchy** — Evaluate attention, flow, and emphasis using `critique-visual-hierarchy` skill.
3. **Composition** — Evaluate balance, whitespace, rhythm, and gestalt using `critique-composition` skill.
4. **Typography** — Evaluate scale, readability, and consistency using `critique-typography` skill.
5. **Brand consistency** — If context files are present, evaluate alignment using `critique-brand-consistency` skill.
6. **Priority order** — Rank all findings by impact: what to fix first, what to fix later, what to leave.

## Output

Full critique report with findings per dimension, specific issues with named elements, and a prioritised fix list.
Consider following up with `/design-screen` to implement the recommended changes.
