---
name: analyze-aged-receivables
description: Build an aged receivables analysis from unpaid invoices and customer balances. Use for an aging balance, overdue buckets, late-payment exposure, top overdue customers, or prioritization by days overdue.
---

# Analyze Aged Receivables

1. Resolve the organization only when needed, then use `list-invoices` for issued and overdue invoices with a remaining amount. Continue through all relevant pages.
2. Compare each due date with today's date and group remaining amounts into not due, 1 to 30 days overdue, 31 to 60 days, 61 to 90 days, and more than 90 days.
3. Use `list-customer-balances` to reconcile portfolio totals and rank customer exposure. Explain any difference caused by filters, pagination, credits, or data timing.
4. Present totals and percentages by aging group, the largest customer exposures, the oldest invoices, and the recommended priorities.

Keep this workflow read-only. Respond in the language of the user's latest request. Copy proper names exactly. Never expose technical identifiers. Use natural business vocabulary and avoid internal terminology.
