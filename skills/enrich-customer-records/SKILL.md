---
name: enrich-customer-records
description: Add customer contacts or invoices to Billabex from complete user-provided data and documents. Use for enriching an account, adding a debtor contact, or importing a missing invoice.
---

# Enrich Customer Records

1. Resolve the organization if needed and identify exactly one customer with `list-accounts`.
2. Check existing data with `list-contacts` or `list-invoices` to prevent obvious duplicates.
3. For a contact, require the exact full name and two-letter language code. Use `create-contact` only after the user confirms the account and values.
4. For an invoice, follow the `import-invoice` skill: it also covers a customer that does not exist yet.
5. Never guess missing financial data, dates, language, currency, customer, or document references. Summarize the created record without exposing technical identifiers.

Respond in the language of the user's latest request. Copy proper names exactly. Use natural business vocabulary and avoid internal terminology.
