---
name: analyze-receivables-statistics
description: Calculate useful Billabex receivables statistics from customer balances, invoices, communications, and tasks. Use for portfolio KPIs, outstanding totals, overdue rates, payment follow-up activity, customer concentration, or management reporting.
---

# Analyze Receivables Statistics

1. Resolve the organization with `list-organizations` only when needed.
2. Use `list-customer-balances` for account exposure and `list-invoices` for invoice counts, amounts, payment status, and overdue status. Use `list-communications` and `list-account-tasks` only when the requested statistics require them.
3. Continue through every relevant page before calculating a portfolio-wide result. If complete pagination is not practical, label the result as a partial sample.
4. Calculate only metrics supported by retrieved fields. Never infer a payment date, recovery rate, trend, or historical comparison from current-state data alone.
5. Present the requested KPIs first, followed by concentration risks, notable exceptions, the covered period, and the calculation basis.

Keep this workflow read-only. Respond in the language of the user's latest request. Copy proper names exactly. Never expose technical identifiers. Use natural business vocabulary and avoid internal terminology.
