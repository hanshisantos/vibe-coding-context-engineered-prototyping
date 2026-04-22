---
marp: true
theme: default
paginate: true
header: "Vibe Coding: Context-Engineered Prototyping"
footer: "Santos Martinez | @hanshisantos"
style: |
  section {
    font-family: 'Segoe UI', sans-serif;
  }
  h1 {
    color: #1a1a2e;
  }
  h2 {
    color: #16213e;
  }
  .highlight {
    color: #e94560;
    font-weight: bold;
  }
---

# Vibe Coding
## A Practical Guide to Context-Engineered Prototyping

**Santos Martinez**
Principal Product Manager Architect, Microsoft CXE

---

# What We Will Cover Today

1. Why context matters in AI interactions
2. The VIBE Loop framework
3. Hands-on: Define your vibe
4. Live demo: Transform a prompt with context engineering
5. Hands-on: Build your own context-engineered prompt
6. Security and responsible AI guardrails
7. Rapid prototyping demo
8. Q&A

---

# The Problem: Context Gets Lost

When we interact with AI, we lose something critical:

- **Cultural identity** gets flattened into generic responses
- **Emotional tone** gets replaced with corporate neutrality
- **Experiential knowledge** gets ignored for textbook answers
- **Intent** gets misread because we never stated it

The result? AI outputs that are technically correct but contextually wrong.

---

# What Is Vibe Coding?

**Vibe Coding** is the practice of designing AI interactions that preserve the cultural, emotional, and experiential context of the person behind the prompt.

It is not about writing longer prompts.
It is about writing *intentional* prompts.

> "The vibe is the context that numbers cannot capture."

---

# Why Does This Matter?

| Without Context Engineering | With Context Engineering |
|---|---|
| Generic, one-size-fits-all outputs | Responses aligned with your identity |
| Misunderstood intent | Clear, purpose-driven interactions |
| Unsafe or biased patterns | Built-in guardrails from the start |
| Throwaway prototypes | Reusable interaction patterns |

---

# Real-World Example

**Naive prompt:**
> "Write me a business email."

**Context-engineered prompt:**
> "I am a senior technical leader writing to a cross-functional team after a missed deadline. My communication style is direct but respectful. The team is demoralized. I need to acknowledge the miss, redirect focus to next steps, and restore confidence without assigning blame."

Same task. Completely different output.

---

<!-- _class: lead -->

# The VIBE Loop

---

# The VIBE Loop Framework

A repeatable process for engineering context into every AI interaction.

| Letter | Element | Question to Ask |
|---|---|---|
| **V** | Value | What matters most in this interaction? |
| **I** | Intent | What outcome am I trying to achieve? |
| **B** | Boundaries | What should the AI *not* do? |
| **E** | Expression | How should the response sound and feel? |

---

# V — Value

**What matters most in this interaction?**

This is about *priorities*, not features.

Examples:
- "Accuracy matters more than speed"
- "Cultural sensitivity is non-negotiable"
- "Preserving the original author's voice is the priority"

**Exercise question:** What is the one thing that, if the AI gets wrong, makes the entire output useless?

---

# I — Intent

**What outcome am I trying to achieve?**

Be specific. "Help me write" is not an intent.

Examples:
- "Persuade a skeptical executive to fund this project"
- "Teach a junior engineer this concept without jargon"
- "Draft a response that de-escalates a frustrated customer"

**Exercise question:** If the AI succeeds perfectly, what changes in the real world?

---

# B — Boundaries

**What should the AI not do?**

Boundaries are your safety net. They prevent:
- Hallucinated data presented as fact
- Tone-deaf or culturally inappropriate responses
- Scope creep beyond the task
- Security and privacy violations

Examples:
- "Do not fabricate statistics or citations"
- "Do not use casual language in this legal context"
- "Do not include PII or internal project names"

---

# E — Expression

**How should the response sound and feel?**

This is where the *vibe* lives.

Examples:
- "Conversational but authoritative, like a trusted mentor"
- "Technical and precise, written for a peer reviewer"
- "Warm and encouraging, written for first-generation college students"

**Exercise question:** If you read this output aloud, would it sound like *you*?

---

<!-- _class: lead -->

# Exercise 1: Define Your Vibe
### (6 minutes)

---

# Exercise 1: Define Your Vibe

Open `exercises/01-define-your-vibe/vibe-worksheet.md`

**Instructions:**
1. Pick a task you actually need AI help with this week
2. Fill in each section of the VIBE worksheet
3. Do not overthink it. First instinct is fine.

| Element | Your Answer |
|---|---|
| **V** — Value | What matters most? |
| **I** — Intent | What real-world outcome? |
| **B** — Boundaries | What must the AI avoid? |
| **E** — Expression | How should it sound? |

---

<!-- _class: lead -->

# Live Demo
### From VIBE to Context-Engineered Prompt

---

# Demo: The Transformation

We will take a real task and walk through:

1. **Start with a naive prompt** (what most people write)
2. **Apply the VIBE Loop** (ask the four questions)
3. **Build the context-engineered prompt** (structured, intentional)
4. **Compare the outputs** (side by side)
5. **Add guardrails** (security and responsible AI boundaries)

Watch how each VIBE element changes the AI's behavior.

---

# Demo: Naive Prompt

```
Summarize this quarterly report for my team.
```

What could go wrong?
- Wrong audience level
- Wrong tone
- Key details omitted
- Sensitive data exposed

---

# Demo: After the VIBE Loop

```
You are helping a senior PM summarize a quarterly report
for a cross-functional team of engineers and designers.

Value: Highlight decisions that affect the next sprint.
       Accuracy over completeness.

Intent: The team should leave the meeting knowing exactly
        what changed and what they need to do next.

Boundaries: Do not include revenue figures or customer names.
            Do not speculate beyond what the report states.

Expression: Direct and concise. Use bullet points.
            Tone is collaborative, not executive.
```

---

# Demo: The Output Difference

| Naive Prompt Output | Context-Engineered Output |
|---|---|
| Generic executive summary | Sprint-focused action items |
| Includes sensitive revenue data | Revenue figures excluded |
| Formal corporate tone | Collaborative team tone |
| Buries the actionable items | Leads with what changed |

The prompt did not get longer for the sake of length. Every line serves a purpose.

---

<!-- _class: lead -->

# Exercise 2: Build Your Prompt
### (12 minutes)

---

# Exercise 2: Build Your Context-Engineered Prompt

Open `exercises/02-build-your-prompt/`

**Instructions:**
1. Start with the naive prompt in `before-prompt.md`
2. Apply your VIBE Loop answers from Exercise 1
3. Write your context-engineered prompt in `after-prompt.md`
4. If you have access to an AI tool, test both prompts and compare

**Checklist:**
- [ ] Value is stated explicitly
- [ ] Intent describes a real-world outcome
- [ ] At least one boundary is defined
- [ ] Expression matches your authentic voice

---

<!-- _class: lead -->

# Security and Responsible AI

---

# Guardrails Are Not Optional

Context engineering includes knowing what to *exclude*.

**Security considerations:**
- Never embed credentials, API keys, or tokens in prompts
- Avoid including PII (names, emails, internal IDs) in shared prompts
- Treat prompt templates like code: review, version, protect

**Responsible AI considerations:**
- State boundaries explicitly; do not assume the model knows your limits
- Test for bias: does the output change unfairly based on cultural markers?
- Verify factual claims; context engineering does not prevent hallucination

---

# The Guardrail Layer

Add this to any context-engineered prompt:

```
Safety and Boundaries:
- Do not fabricate data, citations, or statistics.
- Do not include personally identifiable information.
- If uncertain, state the uncertainty explicitly.
- Flag any content that could be interpreted as biased
  or culturally insensitive.
- This prompt and its outputs should not be shared
  outside [defined audience].
```

This is your **minimum viable guardrail**. Customize per use case.

---

<!-- _class: lead -->

# Rapid Prototyping Demo

---

# From Prompt to Prototype in Minutes

Context-engineered prompts become reusable artifacts:

1. **Prompt Template** — Parameterized VIBE-structured prompt
2. **Interaction Pattern** — Multi-turn conversation design
3. **Lightweight Prototype** — Working demo with guardrails

```
Template: Customer Onboarding Assistant
Parameters: {product_name}, {audience_level}, {tone}
VIBE:
  V: New users complete setup without support tickets
  I: Guide through first 3 steps with zero jargon
  B: No upselling, no feature comparisons
  E: Patient, encouraging, like a helpful colleague
```

---

# When to Prototype vs. When to Ship

| Prototype | Production |
|---|---|
| Test the VIBE alignment | Harden the guardrails |
| Validate with 3-5 users | Monitor for drift |
| Iterate on expression | Add logging and feedback loops |
| Break things safely | Version and audit prompts |

**Rule of thumb:** If you cannot explain the VIBE Loop for your prompt, it is not ready for production.

---

# Take-Home: Exercise 3

Open `exercises/03-rapid-prototype/`

Build a prototype prompt template for one of these scenarios:
- A study buddy that matches your learning style
- A code reviewer that respects your team's conventions
- A writing assistant that preserves your cultural voice

Use the template provided. Apply the full VIBE Loop.

---

<!-- _class: lead -->

# Wrap-Up

---

# What You Learned Today

1. **Vibe Coding** — designing AI interactions that preserve context
2. **The VIBE Loop** — Value, Intent, Boundaries, Expression
3. **Context engineering** — structured prompts that align AI with human intent
4. **Guardrails** — security and responsible AI are part of the design, not an afterthought
5. **Rapid prototyping** — turning prompts into reusable, testable artifacts

---

# Your Next Steps

- [ ] Apply the VIBE Loop to one real task this week
- [ ] Share your prompt template with a colleague and get feedback
- [ ] Add guardrails to every prompt you write from now on
- [ ] Complete Exercise 3 (rapid prototype) on your own time
- [ ] Explore the resources in the `resources/` folder

**Repository:** github.com/hanshisantos/vibe-coding-context-engineered-prototyping

---

<!-- _class: lead -->

# Q&A
### 10 Minutes

What questions do you have?

---

# Thank You

**Santos Martinez**
Principal Product Manager Architect, Microsoft CXE

**Repository:** github.com/hanshisantos/vibe-coding-context-engineered-prototyping

**Connect:** @hanshisantos

> "The best AI interactions start with knowing what matters to you."
