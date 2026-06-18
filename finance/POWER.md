---
name: "finance"
displayName: "Finance"
description: "Finance and accounting workflows for journal entries, reconciliations, close management, financial statements, variance analysis, and SOX audit support."
keywords: ["finance", "accounting", "journal-entries", "reconciliation", "close-management", "financial-statements", "variance-analysis", "sox", "audit"]
author: "Anthropic"
---

# Finance

Guided finance and accounting power for operational accounting, close management, reporting, and audit preparation. It works as a standalone knowledge power when you provide balances, schedules, statements, or workpapers directly, and it becomes more effective when connected to financial data sources through MCP.

This power assists with finance and accounting workflows but does not provide financial, tax, legal, or audit advice. Outputs should be reviewed by qualified professionals before use in reporting, filings, or audit documentation.

## Steering Index

- `steering/journal-entry-preparation.md`: Prepare journal entries with debits, credits, supporting detail, and review checks.
- `steering/journal-entry-guidance.md`: Reference best practices, entry types, documentation standards, and approval workflows.
- `steering/reconciliation.md`: Reconcile GL balances against subledgers, banks, and third-party balances.
- `steering/financial-statements.md`: Generate financial statements with comparisons, variance flags, and GAAP-oriented presentation guidance.
- `steering/variance-analysis.md`: Decompose financial variances into drivers, narratives, and waterfall views.
- `steering/close-management.md`: Run the month-end close with sequencing, dependencies, and status tracking.
- `steering/audit-support.md`: Support SOX 404 and audit workpapers with testing, evidence, and deficiency evaluation.
- `steering/sox-testing.md`: Generate control matrices, sample selections, and testing workpaper templates.

## When To Use Which Workflow

- Use `journal-entry-preparation.md` when you need a formatted entry for accruals, depreciation, prepaids, payroll, or revenue adjustments.
- Use `journal-entry-guidance.md` when you need accounting treatment patterns, support requirements, or approval and review controls.
- Use `reconciliation.md` when matching GL to subledger, bank, or intercompany balances and tracking reconciling items.
- Use `financial-statements.md` when preparing P&L, balance sheet, or cash flow outputs with comparison periods and flux review.
- Use `variance-analysis.md` when investigating budget, forecast, or period-over-period movements and writing management commentary.
- Use `close-management.md` when planning or running the close calendar and tracking blockers across T+1 to T+5.
- Use `audit-support.md` when documenting controls, sampling logic, evidence requirements, or deficiency severity.
- Use `sox-testing.md` when building repeatable control testing packages for quarterly or annual SOX work.

## Standalone Versus Supercharged

This power works without MCP:

- Paste trial balances, subledger exports, schedules, or statements directly.
- Upload spreadsheets or summarize the accounting issue in plain language.
- Ask for formatted outputs such as journal entries, reconciliations, workpapers, close checklists, or variance narratives.

With MCP connected, it can gather data more directly:

- ERP or accounting systems: source balances, journal entries, subledger detail, and period-end data.
- Data warehouses: historical comparisons, variance analysis, and rollups from financial datasets.
- Chat tools: close-status communication and follow-up coordination.

See `mcp.json` for optional integrations. Included servers are disabled by default so you can opt in explicitly.

## Best Practices

- Review all generated outputs before posting entries, closing books, or sharing audit evidence.
- Provide exact periods, account scopes, thresholds, and comparison bases so the output matches the reporting need.
- Keep supporting documentation and assumptions explicit, especially for estimates, accruals, and narratives.
- Distinguish timing differences from true adjustments during reconciliations and close review.
- Use materiality thresholds consistently across statement review, variance analysis, and control testing.
