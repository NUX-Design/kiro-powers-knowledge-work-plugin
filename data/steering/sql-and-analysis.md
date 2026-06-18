# SQL, Data Exploration & Analysis

SQL best practices, query writing, data exploration, and end-to-end analysis workflows.

## Writing SQL Queries

When asked to write SQL, follow this workflow:

1. **Parse the request** - identify output columns, filters, aggregations, joins, ordering, limits
2. **Determine dialect** - PostgreSQL, Snowflake, BigQuery, Redshift, Databricks, MySQL, DuckDB, SQLite
3. **Discover schema** - if warehouse MCP is connected, search relevant tables and inspect columns
4. **Write the query** following best practices below
5. **Present** with explanation, performance notes, and modification suggestions
6. **Offer to execute** if warehouse is connected

### SQL Best Practices

**Structure:**
- Use CTEs for readability; one CTE per logical transformation
- Name CTEs descriptively (`daily_signups`, `active_users`, `revenue_by_product`)

**Performance:**
- Never `SELECT *` in production - specify needed columns only
- Filter early - push WHERE clauses close to base tables
- Use partition filters (especially date partitions)
- Prefer `EXISTS` over `IN` for large subqueries
- Use appropriate JOIN types; avoid LEFT JOIN when INNER is correct
- Be mindful of exploding many-to-many joins

**Readability:**
- Comment the "why" for non-obvious logic
- Consistent indentation
- Meaningful table aliases (not `a`, `b`, `c`)

### Dialect Quick Reference

**PostgreSQL:** `DATE_TRUNC('month', col)`, `ILIKE`, `col::DATE`, `data->>'key'`
**Snowflake:** `DATEADD(day, 7, col)`, `DATEDIFF(day, start, end)`, `col:key::STRING`, `LATERAL FLATTEN()`
**BigQuery:** `DATE_TRUNC(col, MONTH)`, `LOWER(col) LIKE` (no ILIKE), `UNNEST()`, `SAFE_DIVIDE()`
**Redshift:** `DATEADD(day, 7, col)`, `LISTAGG()`, use DISTKEY/SORTKEY
**Databricks:** `DATE_ADD(col, 7)`, Delta Lake time travel, `MERGE INTO`

### Common SQL Patterns

**Window functions:**
```sql
ROW_NUMBER() OVER (PARTITION BY user_id ORDER BY created_at DESC)
SUM(revenue) OVER (ORDER BY date ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW)
LAG(value, 1) OVER (PARTITION BY entity ORDER BY date) as prev_value
revenue / SUM(revenue) OVER () as pct_of_total
```

**Cohort retention:**
```sql
WITH cohorts AS (
  SELECT user_id, DATE_TRUNC('month', first_activity_date) as cohort_month FROM users
),
activity AS (
  SELECT user_id, DATE_TRUNC('month', activity_date) as activity_month FROM user_activity
)
SELECT c.cohort_month, COUNT(DISTINCT c.user_id) as cohort_size,
  COUNT(DISTINCT CASE WHEN a.activity_month = c.cohort_month + INTERVAL '1 month' THEN a.user_id END) as month_1
FROM cohorts c LEFT JOIN activity a ON c.user_id = a.user_id
GROUP BY c.cohort_month ORDER BY 1;
```

**Deduplication:**
```sql
WITH ranked AS (
  SELECT *, ROW_NUMBER() OVER (PARTITION BY entity_id ORDER BY updated_at DESC) as rn
  FROM source_table
)
SELECT * FROM ranked WHERE rn = 1;
```

---

## Exploring Data

When asked to profile or explore a dataset:

### Workflow

1. **Access data** - resolve table name or load file
2. **Understand structure** - row count, grain, primary key, date range, column classification
3. **Generate profile** - nulls, cardinality, distributions, value frequencies
4. **Identify quality issues** - high null rates, duplicates, suspicious values, encoding problems
5. **Discover relationships** - foreign keys, hierarchies, correlations
6. **Recommend follow-ups** - suggest 3-5 specific analyses

### Column Classification

Categorize each column as: Identifier, Dimension, Metric, Temporal, Text, Boolean, or Structural.

### Quality Flags

- >5% nulls: warn | >20% nulls: alert
- Low cardinality on expected high-cardinality columns
- Placeholder values: 0, -1, 999999, "N/A", "TBD", "test"
- Duplicate natural keys
- Extreme distribution skew

### Profile Output Format

```
## Data Profile: [table_name]
### Overview
- Rows: X | Columns: Y (dimensions, metrics, dates, IDs)
- Date range: min to max
### Column Details (summary table)
### Data Quality Issues (flagged with severity)
### Recommended Explorations (numbered list)
```

---

## Analyzing Data

When asked a data question, determine complexity:

- **Quick answer**: Single metric, simple filter → query + direct answer
- **Full analysis**: Multi-dimensional, trends, comparisons → query + charts + patterns
- **Formal report**: Comprehensive investigation → methodology + findings + recommendations

### Analysis Workflow

1. Understand the question (metrics, dimensions, time ranges needed)
2. Gather data (query warehouse, or ask user to provide)
3. Analyze (aggregations, comparisons, patterns, outliers)
4. Validate (row count sanity, null check, magnitude check, trend continuity)
5. Present (lead with key finding, support with evidence)
6. Visualize where helpful

### Validation Before Presenting

Always check:
- Row count makes sense
- No unexpected nulls skewing results
- Numbers in reasonable range
- Time series have no unexpected gaps
- Subtotals sum to totals
