---
name: triage-account-tasks
description: Review tasks created when the autonomous Billabex agent is blocked, explain the missing decision or information, and help the user respond or cancel a task. Use for blocked accounts, pending questions, requested approvals, or task follow-up.
---

# Triage Account Tasks

1. Resolve the organization if needed, find the customer with `list-accounts`, then use `list-account-tasks` and `get-account-task` to inspect tasks created because the agent needs user input.
2. Summarize what is blocking the autonomous payment follow-up, what is requested, why it matters, and the related account or balance context.
3. Prioritize tasks by urgency and financial exposure. Propose the minimum response needed to unblock the agent.
4. Keep the review read-only. Use `add-account-task-text-interaction` only when the user explicitly provides or approves the exact free-form response.
5. After explicit user approval, use the dedicated decision tool matching the task: `decide-account-task-eligibility`, `decide-account-task-contact-change`, `decide-account-task-first-outreach`, `provide-account-task-contact`, `decide-account-task-next-action`, `decide-account-task-payment-arrangement`, `decide-account-task-email-draft`, `confirm-account-task-recipients`, `confirm-account-task-resume`, or `acknowledge-unknown-account-task`. Read its input schema and pass `accountTaskId` and the approved `value`. Never invent a decision or use a tool absent from the connected server. The tool only confirms that the response was recorded: read `get-account-task` to report the task's new state.
6. Use `cancel-account-task` only after an explicit request. Never bypass its confirmation.

Respond in the language of the user's latest request. Copy proper names exactly. Never expose technical identifiers. Use natural business vocabulary and avoid internal terminology.
