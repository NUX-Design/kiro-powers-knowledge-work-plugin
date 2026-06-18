# Business Briefs

Use this workflow for concise owner briefings such as a Monday snapshot, Friday recap, or broader business pulse.

This steering file merges the source plugin’s:

- `business-pulse`
- plus wrapper-style `monday-brief`, `friday-brief`, and related review flows

## Modes

### Business pulse

Run for:

- how is the business doing
- snapshot
- what am I missing
- catch me up

Workflow:

1. Pull all available data sources in parallel.
2. Compute key finance, sales, pipeline, and urgency metrics.
3. Flag record-specific risks.
4. Synthesize to the single most important thing the owner needs to act on today.

Rules:

- Do not block the whole brief on one broken connector.
- Use deltas vs prior periods whenever possible.
- Include only sections with real data.

### Monday brief

Run for:

- monday brief
- start of week
- what is on my plate

Workflow:

1. Pull the broader business pulse.
2. Format a one-screen Monday brief including:
   - cash
   - sales trend
   - pipeline
   - week-ahead commitments
   - top three actions
3. Optionally save it to files or desktop.
4. Optionally post a shortened version to Slack after confirmation.

### Friday brief

Run for:

- end of week
- friday recap
- how did we do

Workflow:

1. Pull revenue and close activity from connected sources.
2. Summarize wins, watches, revenue delta, and top movers.
3. Offer save/post options after the owner sees the summary.

## Output Guidance

Keep briefs fast to scan. Prefer:

- clear headings
- concrete dollars and counts
- week-over-week or month-over-month deltas
- names of records, customers, or deals when action is needed

## Guardrails

- Never invent missing numbers.
- Never auto-post externally without confirmation.
- If a connector is missing, say what was skipped rather than hiding it.

