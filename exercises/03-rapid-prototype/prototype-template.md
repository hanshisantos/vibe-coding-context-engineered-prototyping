# Rapid Prototype Template

Use this template to build a reusable, context-engineered prompt prototype.

---

## Prototype Name

> [Give your prototype a descriptive name, e.g., "Sprint Standup Summarizer"]

## Scenario

> [Describe the situation where this prototype would be used]

## Target User

> [Who will use this template? You? Your team? Students?]

---

## VIBE Configuration

### Value
> [What matters most every time this template is used?]

### Intent
> [What real-world outcome should this consistently produce?]

### Boundaries
> [What must the AI always avoid in this context?]

### Expression
> [What voice, tone, and style should the output have?]

---

## Prompt Template

```
[System/Role Context]
You are a {role} helping {audience} with {task}.

[Value]
Priority: {what matters most}

[Intent]
Goal: {specific real-world outcome}

[Boundaries]
- Do not {boundary_1}
- Do not {boundary_2}
- Do not {boundary_3}

[Expression]
Tone: {voice and style description}

[Safety and Guardrails]
- Do not fabricate data, citations, or statistics.
- Do not include personally identifiable information.
- If uncertain, state the uncertainty explicitly.
- Flag any content that could be biased or culturally insensitive.

[The Task]
{user_input_goes_here}
```

---

## Parameters

List the variables in your template that change per use:

| Parameter | Description | Example |
|---|---|---|
| `{role}` | | |
| `{audience}` | | |
| `{task}` | | |
| `{user_input_goes_here}` | | |

---

## Test Results

### Test 1
**Input:** [What you provided]
**Output quality:** [Rate 1-5 and note what worked/failed]
**Refinement:** [What you changed]

### Test 2
**Input:** [Second test]
**Output quality:** [Rate 1-5]
**Refinement:** [What you changed]

---

## Iteration Notes

> [What did you learn from testing? What would you change for v2?]
