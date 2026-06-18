---
name: "small-business"
displayName: "Small Business"
description: "Operational workflows for small business owners across cash flow, month-end close, taxes, sales, marketing, customer support, CRM hygiene, hiring, contracts, onboarding, and weekly business snapshots."
keywords: ["smb", "small-business", "finance", "marketing", "crm", "customer-support", "contracts", "hiring", "operations"]
author: "NUX DESIGN"
---

# Small Business Power

A small-business operations power for Kiro. It packages practical owner workflows across finance, sales, marketing, customer operations, hiring, contracts, and weekly business visibility, with explicit approval gates before any external or money-touching action.

The source plugin uses two layers: atomic skills and command-style wrappers that chain those skills together. This Kiro conversion merges those artificial splits into fewer steering files so the workflows stay readable while preserving the original orchestration logic, guardrails, and approval checkpoints.

## Available Steering Files

| File | Use When |
|------|----------|
| `setup-and-routing.md` | Getting started, choosing connectors, storing business context, or routing an open-ended owner request to the right workflow |
| `cash-and-finance.md` | Forecasting cash, chasing invoices, checking margins, closing the month, or preparing accountant-ready tax materials |
| `sales-and-marketing.md` | Prioritizing leads, generating content strategy, building Canva-backed campaigns, or running a sales brief |
| `customer-operations.md` | Reviewing customer sentiment, handling complaints, or keeping HubSpot records current |
| `contracts.md` | Reviewing NDAs, MSAs, vendor agreements, or other small-business contracts in plain English |
| `hiring.md` | Producing hiring packets with job posts, interview guides, rubrics, and offer-letter templates |
| `business-briefs.md` | Producing Monday, Friday, or broader business-pulse briefings across the company’s connected tools |

## When to Use Each Workflow

- Use `setup-and-routing.md` when the owner is new, unsure what to run, or needs help connecting the first useful tools.
- Use `cash-and-finance.md` when the concern is payroll confidence, cash crunches, overdue invoices, pricing pressure, month-end close, or tax prep.
- Use `sales-and-marketing.md` when the business needs more pipeline, better lead focus, or a campaign built from current sales signals.
- Use `customer-operations.md` when customers are unhappy, trends in complaints need synthesis, or CRM hygiene is decaying.
- Use `contracts.md` when a contract needs plain-English review, risk flagging, or suggested redlines.
- Use `hiring.md` when the owner needs a complete recruiting packet but not applicant screening.
- Use `business-briefs.md` when the owner wants a one-page business snapshot or recurring check-in.

## Standalone vs Supercharged

The power works without every connector, but it becomes meaningfully better as more systems are connected:

| Workflow | Standalone | Supercharged With |
|----------|-----------|-------------------|
| Finance | CSVs, pasted numbers, uploaded documents | QuickBooks, PayPal, Stripe, Square |
| Sales & marketing | Pasted pipeline or sales notes | HubSpot, QuickBooks, PayPal, Canva, Gmail, Calendar |
| Customer ops | Pasted emails or ticket text | PayPal, HubSpot, Gmail, Intercom |
| Contracts | File upload or pasted text | Gmail, DocuSign |
| Hiring | Conversation-only hiring brief | Google Drive, DocuSign, web research |
| Business briefs | Manual status summary | QuickBooks, PayPal, HubSpot, Gmail, Slack, Calendar |
| Routing & onboarding | Conversation-only | Any connected tool sharpens recommendations |

## Optional MCP Integrations

These integrations materially affect the usefulness of the resulting power, so they are included as disabled-by-default opt-ins:

| Category | Examples | What It Enables |
|----------|----------|-----------------|
| Accounting | QuickBooks | AR/AP, P&L, cash balance, COGS, month-end reconciliation |
| Payments | PayPal, Stripe, Square | Settlement timing, transaction data, disputes, refunds, sales trends |
| CRM | HubSpot | Lead scoring, deal hygiene, pipeline briefs, customer context |
| Marketing design | Canva | Social-asset generation from approved campaign briefs |
| Contracts | DocuSign | Pending-envelope contract review and offer-letter routing |
| Communication | Gmail, Slack | Complaint handling, watch lists, reminder drafts, business briefs |
| Calendar | Google Calendar | Call blocks, meeting context, week-ahead views |
| Files | Google Drive | Templates, saved reports, close packets |

See [mcp.json](/Users/Niwat.yah/Kiro Powers/small-business/mcp.json). All servers are disabled by default so users opt in explicitly.

## Best Practices

1. Treat outputs as owner-support tools, not professional tax, legal, HR, or accounting advice.
2. Keep approval gates intact. Draft, stage, and summarize first; only act externally after explicit confirmation.
3. Prefer business-specific context. Industry, margin structure, seasonality, and customer profile materially change the right advice.
4. When data is missing or a connector is down, surface the gap clearly rather than guessing.
5. Use the router/onboarding workflow early. The plugin is strongest once it knows the business context and the top two connected systems.
