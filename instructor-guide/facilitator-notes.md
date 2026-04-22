# Facilitator Notes

## Workshop: Vibe Coding — A Practical Guide to Context-Engineered Prototyping

**Duration:** 60 minutes + 10-minute Q&A
**Format:** Trainer-led with hands-on exercises
**Materials:** All files in this repository

---

## Before the Session

### Room Setup
- Projector or screen share for slides and live demo
- Participants need a laptop or tablet with browser access
- Wi-Fi access confirmed and tested
- Repository URL on the board or in chat: `github.com/hanshisantos/vibe-coding-context-engineered-prototyping`

### Participant Prerequisites
- See `SETUP.md` in the repository root
- Send the SETUP.md link 24 hours before the session
- Have a fallback plan: printed worksheets or shared Google Doc

### Trainer Prep
- Test the live demo end-to-end with your chosen AI tool
- Have pre-generated outputs saved in case the AI tool is unavailable
- Review all three examples in `examples/` for discussion points
- Prepare 2-3 personal anecdotes connecting VIBE to your PM/security experience

---

## Session Timeline

### Block 1: Welcome and Context (8 minutes)

**Slides 1-6**

**Talking points:**
- Start with the real-world example (slide 6): read both prompts aloud. Let the difference land.
- Ask the room: "How many of you have gotten an AI output that was technically correct but completely useless?" (hands go up)
- Connect to the core problem: context gets lost because we never engineer it in.

**Transition:** "So how do we fix this? With a framework I call the VIBE Loop."

---

### Block 2: The VIBE Loop Framework (8 minutes)

**Slides 7-12**

**Talking points:**
- Walk through each letter with the exercise questions on each slide
- For Boundaries: pause here. This is where security lives. "Boundaries are not just about tone. They are your security perimeter."
- For Expression: ask one participant to describe how they write emails. Use their answer as a live Expression example.

**Transition:** "Now it is your turn. Let's see what your VIBE looks like."

---

### Block 3: Exercise 1 — Define Your Vibe (6 minutes)

**Participants open:** `exercises/01-define-your-vibe/vibe-worksheet.md`

**Facilitation:**
- Set a timer visible to the room: 6 minutes
- Walk the room while they work. Answer questions quietly.
- At the 4-minute mark, announce: "If you are still on Value, that is fine. Move to Intent. You can come back."
- At 6 minutes: "Pens down. You do not need a perfect worksheet. You need a starting point."

**Optional:** Ask 1-2 volunteers to share their Value statement. 30 seconds each.

**Transition:** "Now I am going to show you what happens when we take a VIBE and turn it into a real prompt."

---

### Block 4: Live Demo — VIBE to Prompt (12 minutes)

**Slides 15-20**

**Demo script:**
1. Show the naive prompt on screen (slide 17)
2. Ask the room: "What could go wrong?" Collect 3-4 answers.
3. Walk through the VIBE Loop for this prompt live, building it on screen
4. Show the context-engineered prompt (slide 18)
5. Run both prompts in your AI tool — side by side
6. Point out specific differences in the output
7. Add the guardrail layer (slide 23) and re-run. Show what changes.

**If the AI tool is unavailable:**
- Use pre-saved outputs from your test run
- Walk through the comparison verbally
- The teaching moment is the prompt construction, not the tool

**Key point to land:** "Every line in the context-engineered prompt serves a purpose. This is not about writing more. It is about writing intentionally."

---

### Block 5: Exercise 2 — Build Your Prompt (12 minutes)

**Participants open:** `exercises/02-build-your-prompt/`

**Facilitation:**
- Set timer: 12 minutes
- First 2 minutes: read `before-prompt.md` and identify what is missing
- Next 8 minutes: write their context-engineered version in `after-prompt.md`
- Last 2 minutes: test it if they have an AI tool, or peer-review with a neighbor

**Walk the room.** Common issues to watch for:
- Boundaries that are too vague ("be appropriate") — push for specifics
- Missing Expression — "How should this sound? If you read it aloud, is it your voice?"
- No guardrails — "Add the minimum viable guardrail. Three lines. No exceptions."

**Transition:** "Now let's talk about the thing most people bolt on at the end but should design from the start."

---

### Block 6: Security and Responsible AI (6 minutes)

**Slides 21-23**

**Talking points:**
- Pull up `examples/example-03-security-boundaries.md` — walk through the naive prompt and show exactly what data would leak
- Show the sanitized version. Point out: the diagnostic value is preserved. The sensitive data is not.
- Reference the `resources/responsible-ai-checklist.md`: "This is your take-home. Run it on every prompt before it goes to production."

**Key point:** "Context engineering is a security practice. The VIBE Loop's Boundaries element is where you enforce your security perimeter."

---

### Block 7: Rapid Prototype Demo (8 minutes)

**Slides 24-26**

**Talking points:**
- Show the prototype template on slide 25
- Walk through one complete example: parameterized prompt with VIBE
- Show the progression: VIBE → prompt → template → reusable prototype
- Mention Exercise 3 as take-home: they have everything they need in the repo

**Transition:** "Let's bring this together."

---

### Block 8: Wrap-Up (5 minutes)

**Slides 27-28**

**Talking points:**
- Recap the 5 things they learned (slide 27)
- Read the next steps aloud (slide 28). Make it concrete: "This week. One task. Apply the VIBE Loop."
- Share the repository URL one more time

---

### Block 9: Q&A (10 minutes)

**Slide 29**

**Seed questions if the room is quiet:**
- "What was the hardest VIBE element to fill out? Why?"
- "Did anyone get a surprising result when they tested their prompt?"
- "How would you apply this to something you are working on this week?"

---

## Troubleshooting

| Problem | Solution |
|---|---|
| Wi-Fi is down | Use printed worksheets. Demo from pre-saved outputs. |
| AI tool is unavailable | Peer review replaces testing. Focus on prompt construction. |
| Participants finish early | Point them to Exercise 3 or the examples folder. |
| Participants are stuck | Pair them with a neighbor. Two vibes are better than one. |
| Time is running short | Cut the rapid prototype demo to 3 minutes (just show the template). Protect Q&A time. |
| Someone asks about a specific AI tool | Keep it tool-agnostic. "The VIBE Loop works with any model. The principles are portable." |
