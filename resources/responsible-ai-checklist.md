# Responsible AI Checklist

Use this checklist before deploying any context-engineered prompt in production or sharing it with others.

---

## Security

- [ ] **No credentials in prompts.** API keys, tokens, passwords, and connection strings have been removed.
- [ ] **No PII in prompts.** Email addresses, names, phone numbers, and identifiers have been sanitized.
- [ ] **No internal infrastructure details.** Hostnames, IP addresses, file paths, and service names are redacted.
- [ ] **Prompt templates are version-controlled.** Treat prompts like code. Track changes.
- [ ] **Access is scoped.** Only authorized users can modify production prompt templates.

---

## Data Privacy

- [ ] **Data minimization.** The prompt contains only the data necessary for the task.
- [ ] **No training data leakage.** Outputs do not expose data from other users or sessions.
- [ ] **Consent is obtained.** If the prompt references another person's data, they have consented to its use.
- [ ] **Retention is defined.** You know how long the AI provider retains your prompts and outputs.

---

## Bias and Fairness

- [ ] **Tested across demographics.** The prompt produces equitable outputs regardless of cultural markers.
- [ ] **No stereotyping.** The output does not reinforce harmful stereotypes about any group.
- [ ] **Cultural context is preserved, not flattened.** The AI respects the user's identity without exoticizing it.
- [ ] **Language is inclusive.** The output does not exclude or alienate any part of the intended audience.

---

## Accuracy and Transparency

- [ ] **No fabricated data.** The prompt explicitly instructs the AI not to invent facts, citations, or statistics.
- [ ] **Uncertainty is flagged.** The AI is instructed to say when it does not know something.
- [ ] **Sources are verifiable.** Any referenced data can be checked by the user.
- [ ] **The output is not presented as human-written when it is not.** Disclosure norms are followed.

---

## Boundaries and Scope

- [ ] **Scope is defined.** The AI knows what is in-bounds and out-of-bounds for this task.
- [ ] **Refusal behavior is tested.** The AI correctly refuses when asked to violate boundaries.
- [ ] **Escalation path exists.** There is a process for when the AI produces harmful or incorrect output.
- [ ] **Override protections are in place.** Users cannot trivially bypass the guardrails.

---

## Operational Readiness

- [ ] **The prompt has been tested.** At least 3 diverse inputs have been run through it.
- [ ] **Edge cases are documented.** Known failure modes are recorded.
- [ ] **Feedback mechanism exists.** Users can report problems with the AI's output.
- [ ] **Monitoring is in place.** Outputs are periodically reviewed for drift, bias, or quality degradation.

---

## Quick Decision Framework

Before using a prompt in production, ask:

1. **Would I be comfortable if this prompt and its output were made public?**
2. **Would the person described in this prompt consent to how they are represented?**
3. **If the AI gets this wrong, what is the worst-case consequence?**
4. **Am I relying on the AI for something that requires human judgment?**

If any answer gives you pause, add another boundary to your VIBE Loop.
