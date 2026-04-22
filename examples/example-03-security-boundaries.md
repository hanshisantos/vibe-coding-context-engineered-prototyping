# Example 3: Security Boundaries in Action

## Scenario

A developer wants to use AI to help debug a production issue. The logs contain customer data, internal service names, and infrastructure details. Without proper boundaries, the prompt becomes a data leak.

## Naive Prompt

```
Here are my production logs. Help me find the bug:

[2024-03-15 14:23:01] ERROR UserService: Failed to process
request for user john.doe@contoso.com (tenant: abc-corp-123)
on node prod-east-07.internal.company.com
Connection to db-primary.internal:5432 timed out after 30s
API key: sk-proj-xxxxxxxxxxxxx
```

## What Goes Wrong

This prompt contains:
- A real customer email address (PII)
- An internal tenant identifier
- Internal infrastructure hostnames
- A database connection string
- An API key

If this prompt goes to any external AI service, you just leaked production data.

## Context-Engineered Prompt

```
I am a backend developer debugging a database timeout in a
microservices architecture. I need help identifying the root cause.

Value: Accuracy of the diagnosis. I need the right debugging steps,
       not generic advice.

Intent: Identify the most likely root cause and give me 3 specific
        things to check, in order of likelihood.

Boundaries:
- I have sanitized the logs below. All names, IDs, and endpoints
  are placeholders.
- Do not ask me to share actual hostnames, credentials, or
  customer data.
- Do not suggest fixes that require production access without
  noting the risk.

Expression: Technical and precise. I am a senior developer.
            Skip the basics.

Sanitized log excerpt:
[TIMESTAMP] ERROR UserService: Failed to process request
for user [REDACTED_EMAIL] (tenant: [REDACTED_TENANT])
on node [REDACTED_HOST]
Connection to [REDACTED_DB]:5432 timed out after 30s

Additional context:
- This started happening after a deployment at [TIMESTAMP - 2h]
- Affects approximately 5% of requests
- Other services connecting to the same database are unaffected
- Connection pool size is set to default (20)

Safety:
- All PII has been removed from this prompt.
- Do not request or generate content containing real credentials.
- Do not suggest sharing logs with external services without
  sanitization.
```

## Why This Works

- **Value** keeps the AI focused on diagnosis quality, not breadth
- **Intent** asks for prioritized, actionable steps, not a textbook explanation
- **Boundaries** establish a security perimeter: the AI knows the data is sanitized and should not request the originals
- **Expression** sets the expertise level so the AI skips "have you tried restarting" advice
- **Sanitized data** preserves the diagnostic value of the logs while removing every piece of sensitive information

## The Security Lesson

Context engineering is also a **security practice**. Every prompt is a potential data boundary. The VIBE Loop's Boundaries element is where you enforce it.

### Before You Prompt Checklist

- [ ] Remove all email addresses, usernames, and names
- [ ] Replace hostnames with placeholders
- [ ] Remove API keys, tokens, and credentials
- [ ] Replace tenant IDs and customer identifiers
- [ ] Remove file paths that reveal internal structure
- [ ] Consider whether the *pattern* of data reveals anything sensitive
