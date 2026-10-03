---
name: adjust-scheduled-follow-ups
description: Review and adjust future Billabex payment follow-up emails for selected customer accounts. Use to change a scheduled send date, recipient, subject, language, wording, or tone before an email is sent.
---

# Adjust Scheduled Follow-ups

1. Resolve the organization if needed, find the customer with `list-accounts`, then use `list-outgoing-communications-by-account` and `get-outgoing-communication` to identify the exact unsent email.
2. Show the customer, current scheduled date, recipients, subject, and content before proposing a change.
3. Treat a tone request as an edit to the selected scheduled emails, not as a persistent account preference. Preserve facts, amounts, invoice references, commitments, and the agent's third-party identity.
4. Preview the exact new date or email content. Do not include a signature because Billabex adds the current agent's signature automatically.
5. Use `update-outgoing-communication` only after explicit approval of the unambiguous email and exact changes. Update multiple emails one by one only when the user clearly approves the full list.
6. If no future email exists, explain that this workflow cannot create one and do not send an immediate email instead.

Respond in the language of the user's latest request. Copy proper names exactly. Never expose technical identifiers. Use natural business vocabulary and avoid internal terminology.
