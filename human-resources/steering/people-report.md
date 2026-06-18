# People Report

Use this workflow to generate workforce reports such as headcount, attrition, diversity, or org-health views.

## Report Types

- headcount
- attrition
- diversity
- org health

## Inputs

Accept:

- uploaded CSVs
- pasted workforce tables
- live employee data if connected

Helpful fields include:

- employee identifiers
- department or team
- title and level
- location
- start and end dates
- manager
- compensation when relevant
- demographics when relevant and appropriate

## Analysis Expectations

Start by clarifying the question the report should answer. Then:

1. Identify the right subset of data.
2. Calculate the relevant metrics.
3. Add narrative context and caveats.
4. Recommend actions based on the data.

## Output Format

```markdown
## People Report: [Type] — [Date]

### Executive Summary
[2 to 3 takeaways]

### Key Metrics
| Metric | Value | Trend |
|---|---|---|
| [metric] | [value] | [trend] |

### Detailed Analysis
[narrative, tables, or chart descriptions]

### Recommendations
- [recommendation]

### Methodology
[calculation notes and caveats]
```

## Guardrails

- Be explicit about methodology.
- Be careful with small-sample interpretations.
- Treat demographic and compensation fields as sensitive.
- Distinguish descriptive trends from causal claims.

