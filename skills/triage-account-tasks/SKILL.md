---
name: triage-account-tasks
description: Review tasks created when the autonomous Billabex agent is blocked, explain the missing decision or information, and help the user respond or cancel a task. Use for blocked accounts, pending questions, requested approvals, or task follow-up.
---

# Triage Account Tasks

1. Resolve the organization if needed, find the customer with `list-accounts`, then use `list-account-tasks` and `get-account-task` to inspect tasks created because the agent needs user input.
2. Summarize what is blocking the autonomous payment follow-up, what is requested, why it matters, and the related account or balance context.
3. Prioritize tasks by urgency and financial exposure. Propose the minimum response needed to unblock the agent.
4. Keep the review read-only. Use `add-account-task-text-interaction` only when the user explicitly provides or approves the exact free-form response.
5. Use `add-account-task-structured-interaction` only when the task provides the exact schema, schema version, and allowed value. Never invent them.
6. Use `cancel-account-task` only after an explicit request. Never bypass its confirmation.

Respond in the language of the user's latest request. Copy proper names exactly. Never expose technical identifiers. Use natural business vocabulary and avoid internal terminology.
