---
name: prepare-daily-receivables-brief
description: Prepare a daily customer receivables brief covering changes from the last 24 hours, open tasks, payments, newly overdue invoices, and today's priorities. Use for daily brief, morning review, or changes since yesterday.
---

# Prepare Daily Receivables Brief

1. Resolve the organization with `list-organizations` only when the context does not identify it.
2. Read the last 24 hours with `list-incoming-communications`, `list-outgoing-communications`, `list-invoices`, `list-account-tasks`, and `list-customer-balances` as needed.
3. Summarize payments received, newly overdue invoices, customer replies, future emails already scheduled by Billabex, and tasks created because the agent needs user input.
4. Rank today's actions by urgency, financial exposure, and what is blocking the autonomous payment follow-up.

Keep this workflow read-only. Call a write tool only after the user explicitly requests that exact action and the target is unambiguous.

Respond in the language of the user's latest request. Copy proper names exactly. Never expose technical identifiers. Use natural business vocabulary and avoid internal terminology.
