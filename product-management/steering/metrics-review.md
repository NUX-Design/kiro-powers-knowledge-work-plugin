# Metrics Review

Use this workflow to review product metrics, interpret changes, and recommend actions.

## Inputs

Gather:

- Time period
- Metrics to review
- Comparison period or targets
- Known events that may affect the numbers

If analytics tools are connected, pull the data. Otherwise accept tables, screenshots, or pasted numbers.

## Metrics Hierarchy

Organize the review around:

- North Star metric
- L1 health metrics such as acquisition, activation, engagement, retention, monetization, and satisfaction
- L2 diagnostic metrics for drill-down

If the hierarchy is not defined, help identify it first.

## Analysis Rules

For each key metric capture:

- Current value
- Previous value
- Change
- Target comparison
- Trend direction
- Notable anomalies

Look for:

- Correlations
- Segment differences
- Leading indicators
- Sustained vs one-time changes

## Output Format

```markdown
## Metrics Review

### Summary
[2 to 3 sentence readout]

### Metric Scorecard
| Metric | Current | Previous | Change | Target | Status |
|---|---|---|---|---|---|
| [metric] | [value] | [value] | [delta] | [target] | [status] |

### Trend Analysis
#### [Metric]
- **What happened:** [change]
- **Likely why:** [reason or uncertainty]
- **Significance:** [meaning]

### Bright Spots
- [positive signal]

### Areas of Concern
- [risk or miss]

### Recommended Actions
1. [action]
2. [action]

### Context and Caveats
- [data quality issue, launch effect, outage, seasonality]
```

## Review Cadence Guidance

- Weekly: anomalies, experiments, fast health checks
- Monthly: trends and progress against goals
- Quarterly: strategic performance and OKR review

## Dashboard Rules

- Favor a small set of actionable metrics.
- Always include context, not just raw numbers.
- Avoid vanity metrics.
- Segment where aggregates hide important movement.
- If a metric misses, recommend a response rather than just reporting it.

