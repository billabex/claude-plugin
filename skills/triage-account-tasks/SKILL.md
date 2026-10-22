---
name: triage-account-tasks
description: Review tasks created when the autonomous Billabex agent is blocked, explain the missing decision or information, and help the user respond or cancel a task. Use for blocked accounts, pending questions, requested approvals, or task follow-up.
---

# Triage Account Tasks

1. Resolve the organization if needed, find the customer with `list-accounts`, then use `list-account-tasks` and `get-account-task` to inspect tasks created because the agent needs user input.
2. Summarize what is blocking the autonomous payment follow-up, what is requested, why it matters, and the related account or balance context.
3. Prioritize tasks by urgency and financial exposure. Propose the minimum response needed to unblock the agent.
4. Keep the review read-only. Use `add-account-task-text-interaction` only for a task asking for information, and only when the user explicitly provides or approves the exact free-form response.
5. When the task expects a decision, answer it with the tool that matches its type as read with `get-account-task`: `decide-account-task-next-action`, `decide-account-task-email-draft`, `decide-account-task-eligibility`, `decide-account-task-contact-change`, `decide-account-task-first-outreach`, `decide-account-task-payment-arrangement`, `confirm-account-task-recipients`, `confirm-account-task-resume`, or `provide-account-task-contact`. Use only values the user explicitly gave or approved, and never infer a decision from free text.
6. Use `set-pending-account-task` when the answer depends on something that has not happened yet, `close-account-task` when the user says the matter was dealt with elsewhere, and `cancel-account-task` only after an explicit request. Never bypass a confirmation.

Respond in the language of the user's latest request. Copy proper names exactly. Never expose technical identifiers. Use natural business vocabulary and avoid internal terminology.
