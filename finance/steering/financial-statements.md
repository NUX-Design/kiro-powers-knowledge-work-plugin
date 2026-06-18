# Financial Statements

Generate financial statements with period-over-period comparison and variance analysis support.

This workflow assists with reporting preparation but does not replace professional review for reporting or filings.

## Typical Inputs

- reporting frequency such as monthly, quarterly, annual, or YTD
- reporting period
- current period data
- comparison period or budget data
- account hierarchy or presentation groupings

If ERP or data warehouse tools are connected, use them to pull statement data and historical comparisons. Otherwise, request pasted balances or spreadsheets.

## Core Workflow

### 1. Gather Financial Data

- current-period balances
- prior-period or prior-year comparisons
- budget or forecast if relevant
- account hierarchy and presentation groupings

### 2. Generate The Statement

Primary output is typically a multi-column income statement with current period, prior period, dollar variance, percentage variance, and budget comparison.

Also support:

- balance sheet reference format
- cash flow reference format
- key margin and ratio summaries

### 3. Variance Review

For each material line:

- calculate dollar variance
- calculate percentage variance
- calculate basis point change for ratios and margins
- flag items above defined thresholds
- identify likely drivers and follow-up needs

### 4. Material Variance Summary

```markdown
| Line Item | Variance ($) | Variance (%) | Direction | Preliminary Driver | Action |
|-----------|-------------|-------------|-----------|-------------------|--------|
| [Item]    | $X,XXX      | X.X%        | Unfav.    | [If known]        | Investigate |
```

## Presentation Guidance

- Present operating and non-operating items separately.
- Keep classification consistent across periods.
- Use current versus non-current structure for balance sheet items.
- Disclose non-GAAP adjustments separately when used.
- Treat taxes, leases, goodwill, and allowances according to the applicable reporting framework.

## Output

Provide:

- formatted financial statement output
- key metrics summary
- material variance listing
- suggested follow-up questions
- optional drill-down areas for deeper analysis
