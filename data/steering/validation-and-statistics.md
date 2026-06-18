# Validation & Statistical Analysis

Pre-delivery QA, statistical methods, outlier detection, and hypothesis testing.

## Validating Analysis Before Sharing

When asked to validate or QA an analysis:

### Workflow

1. **Review methodology** - right question? right data? correct population? fair comparison?
2. **Run QA checklist** - data quality, calculations, reasonableness, presentation
3. **Check common pitfalls** - join explosion, survivorship bias, incomplete periods, denominator shift
4. **Spot-check calculations** - recalculate independently, verify subtotals sum
5. **Assess visualizations** - axes start correctly, scales consistent, titles accurate
6. **Evaluate conclusions** - supported by data? alternatives acknowledged? uncertainty communicated?
7. **Generate confidence assessment** - Ready / Share with caveats / Needs revision

### Pre-Delivery QA Checklist

**Data Quality:**
- [ ] Right tables/sources for this question
- [ ] Data freshness noted
- [ ] No unexpected gaps
- [ ] Null rates checked and handled
- [ ] No double-counting from bad joins
- [ ] Filters correct, no unintended exclusions

**Calculations:**
- [ ] GROUP BY includes all non-aggregated columns
- [ ] Denominators correct and non-zero
- [ ] Date comparisons use same period length
- [ ] JOIN types appropriate (no many-to-many inflation)
- [ ] Metric definitions match stakeholder expectations

**Reasonableness:**
- [ ] Numbers in plausible range
- [ ] No unexplained trend jumps
- [ ] Cross-reference matches known sources
- [ ] Edge cases considered

### Common Pitfalls

| Pitfall | Detection | Prevention |
|---------|-----------|------------|
| **Join explosion** | Row count increases after join | Check counts before/after; use COUNT(DISTINCT) |
| **Survivorship bias** | Only analyzing current entities | Ask "who is NOT in this dataset?" |
| **Incomplete period** | Comparing partial to full period | Filter to complete periods only |
| **Denominator shift** | Rate definition changed between periods | Use consistent definitions |
| **Average of averages** | Groups have different sizes | Always aggregate from raw data |
| **Timezone mismatch** | Different sources use different timezones | Standardize to UTC |
| **Selection bias** | Segments defined by the outcome measured | Define segments by pre-treatment characteristics |

### Confidence Assessment Output

```
## Validation Report
### Overall Assessment: [Ready to share | Share with caveats | Needs revision]
### Issues Found (severity + impact)
### Calculation Spot-Checks
### Required Caveats for Stakeholders
```

---

## Statistical Analysis

### Descriptive Statistics

**Central tendency:** Use mean for symmetric data, median for skewed data. Always report both for business metrics.

**Spread:** Standard deviation (normal data), IQR (skewed data), coefficient of variation (compare across scales).

**Key percentiles:** p1, p5, p25, p50, p75, p90, p95, p99

**Distribution shapes:** Normal, right-skewed, left-skewed, bimodal, uniform, heavy-tailed

### Trend Analysis

**Moving averages:** 7-day (smooths weekly patterns), 28-day (smooths monthly patterns)

**Comparisons:** WoW, MoM, YoY (gold standard for seasonal businesses)

**Growth rates:** Simple: `(current - previous) / previous`, CAGR: `(end/begin)^(1/years) - 1`

**Seasonality:** Check day-of-week and month-of-year averages; always use same-period comparisons

**Forecasting (simple):** Naive, seasonal naive, linear trend, moving average. Always provide ranges, not point estimates.

### Outlier Detection

**Z-score** (normal data): Flag |z| > 3

**IQR method** (robust): Lower = Q1 - 1.5*IQR, Upper = Q3 + 1.5*IQR

**Percentile method**: Flag < p1 or > p99

**Do NOT automatically remove outliers.** Investigate first:
- Data error → fix or remove
- Genuine extreme → keep, use robust statistics
- Different population → segment separately

### Hypothesis Testing

**When to use:** A/B tests, before/after comparisons, segment differences.

| Scenario | Test |
|----------|------|
| Two group means | t-test |
| Two proportions | z-test for proportions |
| Paired measurements | Paired t-test |
| 3+ group means | ANOVA |
| Non-normal data | Mann-Whitney U |
| Category association | Chi-squared |

**Always report:**
- Effect size (how big is the difference?)
- Confidence interval (range of plausible effects)
- Business impact (what does this mean in revenue/users?)
- Sample size adequacy

### Statistical Caution

- **Correlation ≠ causation** - consider reverse causation, confounders, coincidence
- **Multiple comparisons** - testing 20 metrics at p=0.05 yields ~1 false positive
- **Simpson's paradox** - aggregated trends can reverse when segmented
- **Survivorship bias** - you can only analyze entities that "survived" to be in your data
- **False precision** - prefer "4-6%" over "4.73%"
- **Small samples** - note limited power to detect small effects
