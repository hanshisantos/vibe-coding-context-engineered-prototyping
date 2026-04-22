# Example 1: Preserving Cultural Context

## Scenario

A first-generation Latino college student needs help drafting a personal statement. Generic AI produces outputs that erase cultural identity and replace it with standardized academic English.

## Naive Prompt

```
Help me write a college personal statement about overcoming challenges.
```

## What Goes Wrong

The AI produces a polished but generic narrative that could belong to anyone. The cultural specificity, the bilingual household, the community obligation, the navigation between two worlds: all of it vanishes behind safe, sanitized language.

## Context-Engineered Prompt

```
I am a first-generation college student from a Puerto Rican family.
I am writing a personal statement for graduate school admissions.

Value: My cultural background is central to this story, not decoration.
       The committee should understand how my identity shaped my
       intellectual curiosity, not just that I "overcame hardship."

Intent: The admissions committee should see a scholar whose
        perspective adds something they do not already have.

Boundaries:
- Do not use poverty narratives or trauma framing.
- Do not sanitize cultural references into generic "diversity" language.
- Do not remove Spanish words or phrases that carry meaning
  English cannot replicate.
- Do not fabricate experiences.

Expression: Confident and reflective. The voice of someone who has
            done the work and knows their worth. Not humble-bragging.
            Not apologetic. Direct.

Safety:
- Do not include real names, institutions, or identifying details.
- If uncertain about a cultural reference, flag it rather than guessing.
```

## Why This Works

- **Value** centers the cultural identity as the point, not the backdrop
- **Intent** focuses on what the reader should think, not just what the writer should say
- **Boundaries** prevent the most common AI failure: smoothing away the specificity that makes the statement memorable
- **Expression** captures a voice that the student would recognize as their own
