---
name: identify-receivables-risks
description: Identify and prioritize customer receivables risks, including high outstanding balances, silent customers, undelivered emails, and missing information. Use for risk reviews, priority lists, blocked follow-up, or silent customer analysis.
---

# Identify Receivables Risks

1. Resolve the organization with `list-organizations` only when needed.
2. Use `list-customer-balances` for financial exposure and `list-silent-accounts` for customers without replies.
3. Use `list-communications` with delivery status filters to find bounced or complained emails. Use `list-account-tasks` and `list-contacts` to identify missing information or contact blockers.
4. Rank customers by amount at risk, age, silence, delivery failure severity, and unresolved dependency. Give the evidence and one recommended next action for each priority.

Keep this workflow read-only. Call a write tool only after the user explicitly requests that exact action and the target is unambiguous.

Respond in the language of the user's latest request. Copy proper names exactly. Never expose technical identifiers. Use natural business vocabulary and avoid internal terminology.
