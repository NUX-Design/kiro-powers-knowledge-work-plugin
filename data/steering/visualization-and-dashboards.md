# Visualization & Dashboards

Chart selection, Python visualization code patterns, and interactive HTML dashboard construction.

## Chart Selection

| Data Relationship | Best Chart | Alternatives |
|---|---|---|
| Trend over time | Line chart | Area chart |
| Comparison across categories | Bar chart | Horizontal bar (many categories) |
| Ranking | Horizontal bar chart | Dot plot |
| Part-to-whole composition | Stacked bar | Treemap |
| Distribution | Histogram | Box plot, violin plot |
| Correlation (2 vars) | Scatter plot | Bubble chart |
| Correlation (many vars) | Heatmap | Pair plot |
| Geographic | Choropleth map | Bubble map |
| Flow/process | Sankey diagram | Funnel chart |

**Avoid:** Pie charts (>6 categories), 3D charts (always), dual-axis (unless clearly labeled).

## Creating Visualizations

### Workflow

1. Determine data source, chart type, purpose, audience
2. Get data into a DataFrame (query or parse uploaded file)
3. Select chart type (recommend if not specified)
4. Generate code using matplotlib+seaborn (static) or plotly (interactive)
5. Apply design best practices
6. Save as PNG and display

### Python Setup

```python
import matplotlib.pyplot as plt
import seaborn as sns
import pandas as pd

plt.style.use('seaborn-v0_8-whitegrid')
COLORS = ['#4C72B0', '#DD8452', '#55A868', '#C44E52', '#8172B3', '#937860']
```

### Code Requirements

Always include:
- Descriptive title stating the insight (not just the metric)
- Axis labels with units
- Remove top/right spines
- Format numbers: `$1.2M` not `1200000`, `45.2%` not `0.452`
- `plt.tight_layout()` and `plt.savefig('name.png', dpi=150, bbox_inches='tight')`

### Design Principles

**Color:** Colorblind-friendly palette, highlight key data, grey less important data
**Typography:** Insight in title, readable labels (not rotated 90deg), data labels on key points
**Layout:** Sort by value (not alphabetically), appropriate whitespace, legend doesn't obscure data
**Accuracy:** Bar charts start at zero, consistent scales across panels, appropriate precision

### Accessibility

- Never rely on color alone - add patterns, line styles, or labels
- Minimum 10pt text for labels
- Provide alt text describing the key finding
- Test in black and white

---

## Building Dashboards

Generate self-contained HTML files with Chart.js, filters, and professional styling.

### Workflow

1. Understand requirements (purpose, audience, key metrics, filter dimensions)
2. Gather data (query or embed provided data as JSON)
3. Design layout (KPI cards → charts → detail table)
4. Build HTML (structure + CSS + JavaScript + embedded data)
5. Save and open in browser

### Dashboard Layout

```
┌──────────────────────────────────────────────────┐
│  Title                              [Filters ▼]  │
├────────────┬────────────┬────────────┬───────────┤
│  KPI Card  │  KPI Card  │  KPI Card  │ KPI Card  │
├────────────┴────────────┼────────────┴───────────┤
│    Primary Chart        │   Secondary Chart      │
├─────────────────────────┴────────────────────────┤
│    Detail Table (sortable)                       │
└──────────────────────────────────────────────────┘
```

### Technical Stack

- **Charts**: Chart.js 4.x via CDN
- **Styling**: CSS Grid/Flexbox, system fonts, card-based layout
- **Interactivity**: Filter dropdowns that update all charts simultaneously, sortable tables, hover tooltips
- **Data**: Embedded as JSON in the HTML (no external fetches)

### Data Size Guidelines

| Rows | Approach |
|------|----------|
| <1,000 | Embed directly, full interactivity |
| 1K-10K | Embed, pre-aggregate for charts |
| 10K-100K | Pre-aggregate server-side, embed summaries only |
| >100K | Not suitable for client-side; use a BI tool |

### Key Implementation Patterns

**KPI Cards:** Value + label + period-over-period change (positive/negative coloring)

**Filters:** Dropdowns populated from distinct values in data, `onchange` triggers `dashboard.applyFilters()` which updates all charts and tables

**Chart Updates:** Use `chart.update('none')` for instant filter-triggered updates (no animation)

**Number Formatting:** Currency ($1.2M), percentages (45.2%), large numbers (2.3K)

**Sortable Tables:** Click headers to sort, show arrow indicator, limit to 100-200 visible rows with pagination

### Color System

```css
--bg-primary: #f8f9fa;
--bg-card: #ffffff;
--bg-header: #1a1a2e;
--text-primary: #212529;
--text-secondary: #6c757d;
--positive: #28a745;
--negative: #dc3545;
```

### Responsive Design

- KPI grid: `repeat(auto-fit, minmax(200px, 1fr))`
- Charts: `repeat(auto-fit, minmax(400px, 1fr))`
- Mobile: stack to single column at 768px
- Print: hide filters, remove shadows, avoid page breaks in charts
