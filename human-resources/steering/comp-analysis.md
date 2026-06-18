# Compensation Analysis

Use this workflow to benchmark pay, assess band placement, analyze outliers, or model equity and total compensation.

## Entry Points

- single-role benchmarking
- uploaded compensation dataset analysis
- equity modeling

## Inputs

For single-role analysis, gather:

- role
- level
- location
- company stage if relevant

For dataset analysis, gather:

- uploaded comp data or pasted band structure
- what decision the user is trying to make

For equity modeling, gather:

- share or unit count
- price or valuation context
- vesting schedule

## Output Expectations

Provide:

- percentile benchmark table
- base, equity, and total comp view
- location and company-stage context
- band-placement analysis if internal data is supplied
- recommendations and flags

## Output Format

```markdown
## Compensation Analysis: [Scope]

### Market Benchmarks
| Percentile | Base | Equity | Total Comp |
|---|---|---|---|
| 25th | [amount] | [amount] | [amount] |
| 50th | [amount] | [amount] | [amount] |
| 75th | [amount] | [amount] | [amount] |
| 90th | [amount] | [amount] | [amount] |

### Band Analysis
| Employee | Current Base | Band Min | Band Mid | Band Max | Position |
|---|---|---|---|---|---|
| [name] | [amount] | [amount] | [amount] | [amount] | [position] |

### Recommendations
- [recommendation]
```

## Guardrails

- State data sources and freshness clearly.
- Location matters; do not flatten geography away.
- Treat uploaded compensation data as sensitive.
- Separate strong evidence from rough market inference.

