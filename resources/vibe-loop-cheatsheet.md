# VIBE Loop Cheat Sheet

A quick reference for applying context engineering to any AI interaction.

---

## The VIBE Loop

```
┌─────────────────────────────────────────────┐
│                                             │
│   V  →  I  →  B  →  E  →  [Prompt]  →  ?   │
│   │     │     │     │                   │   │
│   │     │     │     │      Compare      │   │
│   │     │     │     │      output       │   │
│   │     │     │     │      to VIBE      │   │
│   │     │     │     │                   │   │
│   └─────┴─────┴─────┴───── Iterate ─────┘   │
│                                             │
└─────────────────────────────────────────────┘
```

---

## V — Value

**Ask:** "What matters most?"

| Good | Bad |
|---|---|
| "Accuracy over speed" | "Make it good" |
| "Cultural sensitivity is non-negotiable" | "Be appropriate" |
| "Preserve the original author's voice" | "Keep it natural" |

---

## I — Intent

**Ask:** "What real-world outcome am I trying to achieve?"

| Good | Bad |
|---|---|
| "Persuade a skeptical VP to fund Q3" | "Help me write a proposal" |
| "Junior dev understands auth flow" | "Explain authentication" |
| "Customer feels heard and gets a fix" | "Reply to complaint" |

---

## B — Boundaries

**Ask:** "What must the AI NOT do?"

| Always Include | Context-Specific |
|---|---|
| No fabricated data or citations | No revenue figures in this summary |
| No PII in prompts or outputs | No casual tone for legal content |
| No credentials or API keys | No scope beyond the sprint |

---

## E — Expression

**Ask:** "How should this sound?"

Use concrete references, not abstract adjectives:

| Concrete (Good) | Abstract (Bad) |
|---|---|
| "Like a coach at halftime" | "Professional" |
| "A senior dev in a code review" | "Technical" |
| "A mentor over coffee" | "Friendly and helpful" |

---

## Minimum Viable Guardrail

Add this to every prompt:

```
- Do not fabricate data, citations, or statistics.
- Do not include personally identifiable information.
- If uncertain, state the uncertainty explicitly.
```

---

## Quick Template

```
[Context: who you are and who the audience is]

Value: [what matters most]
Intent: [what real-world outcome you need]
Boundaries: [what the AI must avoid]
Expression: [how the output should sound]

Safety:
- No fabricated data.
- No PII.
- Flag uncertainty.

[Your actual task here]
```

---

## The Iteration Question

After getting output, ask:

> "Does this sound like me, serve my audience, and respect my boundaries?"

If no → identify which VIBE element failed → adjust → re-prompt.
