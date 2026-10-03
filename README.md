# Billabex for Claude

[Billabex](https://www.billabex.com) is a B2B invoice follow-up and amicable collection platform:
invoices come in from your billing tools, and an AI agent follows up with your customers on your
behalf. This plugin connects Claude to your Billabex workspace so you can review receivables and
steer payment follow-up from a conversation.

![Billabex](assets/logo.png)

## What it contains

- **The Billabex MCP connector** (`https://next.billabex.com/mcp`). Signing in happens in your
  browser through Billabex OAuth; the plugin stores no credential. Every call goes to Billabex's
  own API and only reads or changes data in the workspaces you authorize.
- **Ten skills** that teach Claude the usual receivables workflows:

| Skill | Use it to |
| --- | --- |
| `prepare-daily-receivables-brief` | Get a daily brief: changes since yesterday, alerts, priority actions. |
| `review-customer-account` | Review one customer across invoices, contacts, communications, and tasks. |
| `identify-receivables-risks` | Rank the riskiest customers and explain why. |
| `analyze-receivables-statistics` | Compute portfolio KPIs from balances, invoices, communications, and tasks. |
| `analyze-aged-receivables` | Break down the aged balance by customer and bucket. |
| `triage-account-tasks` | Answer or close the questions the Billabex agent is blocked on. |
| `adjust-scheduled-follow-ups` | Review and edit scheduled follow-up emails. |
| `prepare-payment-follow-up-email` | Draft a payment reminder and send it only after your approval. |
| `control-automatic-payment-follow-up` | Pause or resume automatic follow-up for one customer. |
| `enrich-customer-records` | Add a missing contact or invoice to a customer account. |

Analyses are read-only. Every write (sending a message, pausing follow-up, editing a record)
requires an explicit, unambiguous request from you, and Claude asks for confirmation before
destructive actions.

## Requirements

A Billabex account. You can [create one](https://www.billabex.com) and connect your billing tool
in a few minutes.

## Example prompts

- "Prepare my daily receivables brief."
- "Review the full situation of customer Acme and recommend the next action."
- "Which customers are the most at risk right now, and what should I do first?"

## Data and privacy

The plugin sends nothing anywhere except to the Billabex MCP server above, under your own
authorization. See the [privacy policy](https://www.billabex.com/en/privacy-policy) and
[terms of use](https://www.billabex.com/en/terms-and-conditions-of-use).

## Support

support@billabex.com · [Developer documentation](https://developer.billabex.com/)
