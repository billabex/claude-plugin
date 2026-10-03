---
name: review-customer-account
description: Review one customer account across invoices, credit notes, outstanding balance, contacts, communications, tasks, and the recommended next action. Use for a complete customer situation, account review, or next-step recommendation.
---

# Review Customer Account

1. Resolve the organization if needed, then find the customer with the `query` parameter of `list-accounts`. Ask for clarification when several names match.
2. Use `list-customer-balances` and select the balance whose `accountId` matches the customer. If one exists, pass its `id` to `get-customer-balance` as `balanceId`.
3. Use `get-account`, `list-invoices`, `list-credit-notes`, `list-contacts`, `list-incoming-communications-by-account`, `list-outgoing-communications-by-account`, and `list-account-tasks` as needed.
4. Present the financial position, credits, contacts, communication history, next scheduled email, open tasks, blockers, and payment behavior.
5. Explain what Billabex is currently doing for the account and recommend one clear next action without executing it.

Keep the review read-only. Call a write tool only after the user explicitly requests that exact action. Require a clear target and complete content before any destructive or irreversible action.

Respond in the language of the user's latest request. Copy proper names exactly. Never expose technical identifiers. Use natural business vocabulary and avoid internal terminology.
