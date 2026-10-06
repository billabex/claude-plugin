---
name: import-invoice
description: Import an invoice document into Billabex for payment follow-up, creating the customer account first when it does not exist yet. Use when the user shares an invoice PDF or image, or asks to add, upload or import an invoice.
---

# Import Invoice

1. Resolve the organization if needed. Read the invoice and extract its number, issue date, due date, currency, total amount including tax, tax amount, any amount already paid, and the customer: legal name, SIREN or SIRET, VAT number and billing address. Never guess a missing value: ask for it.
2. Find the customer with the `query` parameter of `list-accounts`, trying the legal name and then a shorter distinctive part of it. When candidates appear, compare their SIREN, VAT number or address with `get-account`. Ask the user to choose when several remain plausible.
3. When no account matches, propose to create one from the invoice: legal name, SIREN, VAT number, billing address and the invoice currency. Call `create-account` only after the user confirms these values. If the organization syncs invoices from a billing tool, say that the customer may simply not be synced yet, and let the user decide.
4. Check for a duplicate with `list-invoices` for that account, filtering `number` equal to the invoice number. If the invoice already exists, show it and stop: never change its number to get around the duplicate.
5. Summarize the customer and invoice values, then generate one UUID `importId` and keep it with exactly the same values for every retry.
6. Call `prepare-invoice-upload` with the `importId` and values, then give the user the link exactly as returned, in full, so they review the details and upload the document themselves. The link expires after 15 minutes and preparing it does not create the invoice. Never invent a download URL or ask for base64. Once the user says the upload is done, confirm it with `list-invoices` filtered on the invoice number before reporting success; if the link failed or expired, prepare a new one with the SAME `importId` and values.
7. Check that the customer has a contact with an email address using `list-contacts`. Without one, Billabex cannot follow up: offer to add one with `create-contact`, using only a name, email and language the user provides.
8. Confirm the import in business terms, without technical identifiers.

Respond in the language of the user's latest request. Copy proper names exactly. Never expose technical identifiers. Use natural business vocabulary and avoid internal terminology.
