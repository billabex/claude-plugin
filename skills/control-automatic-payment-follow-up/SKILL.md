---
name: control-automatic-payment-follow-up
description: Review whether automatic payment follow-up should be paused or resumed for a customer account, explain the impact, and perform the change only on explicit request. Use for pausing reminders, resuming reminders, or checking follow-up blockers.
---

# Control Automatic Payment Follow-up

1. Resolve the organization if needed and identify exactly one customer with `list-accounts`. Ask for clarification when several accounts match.
2. Review the account balance, recent communications, and open tasks as needed to explain the current situation and the likely impact of pausing or resuming automatic payment follow-up.
3. When the user asks for analysis or advice, recommend an action without changing the account. For a suspension, propose the reason that matches the facts.
4. Use `pause-account-dunning` or `resume-account-dunning` only after an explicit request for the unambiguous account. A dated reason requires an explicit future `until`; never invent the date. Never apply the change in bulk or guess the target.
5. Confirm the resulting status and explain the operational effect without exposing technical identifiers.

Respond in the language of the user's latest request. Copy proper names exactly. Use natural business vocabulary and avoid internal terminology.
