# Example 2: Preserving Emotional Tone

## Scenario

A team lead needs to communicate a project delay to their team. The situation is stressful, morale is low, and the message needs to be honest without making things worse. Generic AI produces either robotic status updates or inappropriately cheerful spin.

## Naive Prompt

```
Write a message to my team about a project delay.
```

## What Goes Wrong

The AI produces one of two bad outcomes:
1. A cold, corporate status update that feels like it came from HR
2. An overly positive message that feels dishonest given the situation

Neither matches what the team needs to hear right now.

## Context-Engineered Prompt

```
I lead a team of 8 engineers. We just missed a major milestone
by two weeks due to a dependency that was outside our control.
The team has been working hard and morale is fragile.

Value: Honesty without blame. The team needs to hear the truth
       and know that their effort is recognized.

Intent: After reading this message, the team should feel:
        (1) acknowledged for their work,
        (2) clear on what happens next, and
        (3) confident that leadership is not going to throw them
            under the bus.

Boundaries:
- Do not assign blame to any individual or team.
- Do not minimize the delay or pretend it does not matter.
- Do not use phrases like "exciting opportunity" or "silver lining."
- Do not promise things I cannot deliver (bonuses, timeline changes).

Expression: The tone of a coach at halftime when the team is down
            but not out. Calm, steady, direct. Short sentences.
            No corporate jargon.

Safety:
- Do not reference specific project names or client names.
- Do not include dates or timelines that could be traced.
```

## Why This Works

- **Value** names the emotional core: honesty plus recognition
- **Intent** defines the *feeling* the team should have after reading, not just the information they should receive
- **Boundaries** block the AI's worst instincts: blame-shifting, minimizing, and toxic positivity
- **Expression** uses a concrete metaphor ("coach at halftime") that is easier for the AI to calibrate than abstract adjectives
