# Prompt Patterns Catalog

Reusable patterns for common context-engineered prompting scenarios.

---

## Pattern 1: Role-Audience-Task (RAT)

**When to use:** Any interaction where the AI needs to adopt a perspective.

```
You are a [role] helping [audience] with [task].

Value: [priority]
Intent: [outcome]
Boundaries: [constraints]
Expression: [voice]

[Task details]
```

**Example:**
```
You are a senior security engineer reviewing code
for a team of junior developers.

Value: Catch real vulnerabilities, not style preferences.
Intent: The developer fixes the issue before it ships.
Boundaries: Do not rewrite the code. Point to the line and explain why.
Expression: Direct, educational. No condescension.

Review this pull request: [code]
```

---

## Pattern 2: Before-After Comparison

**When to use:** When you need the AI to transform content from one state to another.

```
Here is the current version: [before]

Transform it to meet these requirements:

Value: [what must improve]
Intent: [what the new version should achieve]
Boundaries: [what must not change]
Expression: [target voice/tone]

Show me the transformed version.
```

---

## Pattern 3: Structured Analysis

**When to use:** When you need the AI to analyze something with specific criteria.

```
Analyze [subject] using these criteria:

Value: [what aspect matters most in the analysis]
Intent: [what decision this analysis will inform]
Boundaries:
- Only use information from [specified sources]
- Do not speculate beyond the data
- Flag assumptions explicitly
Expression: [format and depth expectations]

Provide your analysis in this structure:
1. Summary (3 sentences max)
2. Key findings (bullet points)
3. Risks or gaps
4. Recommended next step
```

---

## Pattern 4: Iterative Refinement

**When to use:** Multi-turn conversations where you refine output step by step.

```
Turn 1 — First draft:
[Standard VIBE prompt]

Turn 2 — Refinement:
The [Value/Intent/Boundary/Expression] element is not right.
Specifically: [what failed]
Adjust by: [specific change]
Keep everything else the same.

Turn 3 — Final check:
Read the output against these criteria:
- Does it match the stated Value? [Y/N]
- Does it achieve the Intent? [Y/N]
- Does it respect all Boundaries? [Y/N]
- Does it match the Expression? [Y/N]
If any answer is N, explain what needs to change.
```

---

## Pattern 5: Guardrail-First Prompt

**When to use:** High-stakes or sensitive interactions where safety comes first.

```
SAFETY REQUIREMENTS (non-negotiable):
- Do not generate [specific prohibited content]
- Do not include [PII/credentials/internal data]
- If any part of this request conflicts with safety,
  refuse that part and explain why

With those guardrails in place:

[Standard VIBE prompt]
```

---

## Pattern 6: Persona Template

**When to use:** When you want consistent AI behavior across multiple interactions.

```
PERSONA DEFINITION:
Name: [descriptive name for this persona]
Role: [what the AI acts as]
Expertise: [domain knowledge to assume]
Communication style: [Expression details]
Hard limits: [Boundaries that never change]

This persona is used for: [context]

---

[Individual task prompt using this persona]
```

---

## Combining Patterns

Patterns are composable. Common combinations:

- **RAT + Guardrail-First** for security-sensitive code review
- **Before-After + Iterative Refinement** for content editing
- **Structured Analysis + Persona** for recurring reports
- **Any pattern + the Minimum Viable Guardrail** (always)
