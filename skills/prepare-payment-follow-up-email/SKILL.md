---
name: prepare-payment-follow-up-email
description: Prepare a professional payment follow-up email from the customer account, invoice, contact, and communication history, and send it only after explicit approval. Use for drafting or sending a payment reminder or customer follow-up.
---

# Prepare Payment Follow-up Email

1. Resolve the organization with `list-organizations` when needed and use `get-organization` to retrieve the current Billabex agent's exact name. Find one customer with `list-accounts`, then review its balance, invoices, contacts, recent communications, and open tasks as needed.
2. Draft a concise, diplomatic email in the current agent's name, as an independent third party acting on behalf of the organization. Use first-person singular and never imply membership in the organization.
3. Copy proper names, invoice references, amounts, currencies, and dates exactly from the retrieved data. Do not invent a deadline or commitment.
4. Do not add a signature because `send-outgoing-communication` adds it automatically.
5. Treat drafting as read-only. Send only after the user explicitly approves the complete recipients, subject, body, and unambiguous customer account.

Respond in the language requested for the email. Otherwise use the language of the user's latest request. Never expose technical identifiers. Use natural business vocabulary and avoid internal terminology.
