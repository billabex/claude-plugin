---
name: enrich-customer-records
description: Add customer contacts or invoices to Billabex from complete user-provided data and documents. Use for enriching an account, adding a debtor contact, or importing a missing invoice.
---

# Enrich Customer Records

1. Resolve the organization if needed and identify exactly one customer with `list-accounts`.
2. Check existing data with `list-contacts` or `list-invoices` to prevent obvious duplicates.
3. For a contact, require the exact full name and two-letter language code. Use `create-contact` only after the user confirms the account and values.
4. For an invoice, require its document, number, issue date, due date, total amount, tax amount, paid amount, and customer account. When all required data is available, generate one UUID `importId` and call `prepare-invoice-upload` with it and the invoice details, then give the secure temporary link to the user so they upload the document themselves. Never invent a download URL or ask the user for base64. Preparing a link does not create the invoice: wait for confirmation or verify with `get-invoice`. Reuse the same import ID and details for retries; inspect an existing invoice instead of changing its number to bypass a duplicate error.
5. Never guess missing financial data, dates, language, currency, customer, or document references. Summarize the created record without exposing technical identifiers.

Respond in the language of the user's latest request. Copy proper names exactly. Use natural business vocabulary and avoid internal terminology.
