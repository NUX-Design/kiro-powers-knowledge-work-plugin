# Sales and Marketing

Use this workflow for pipeline prioritization, content strategy, campaign production, and sales-performance briefs.

This steering file merges the source plugin’s:

- `lead-triage`
- `content-strategy`
- `canva-creator`
- plus orchestration wrappers such as `call-list`, `run-campaign`, and `sales-brief`

## Modes

### Lead prioritization and call list

Run when the owner asks:

- who should I call
- any hot leads
- prioritize leads
- quick pipeline call list

Workflow:

1. Pull eligible leads from HubSpot.
2. Score each lead across engagement, fit, urgency, and recency.
3. Produce a ranked list sized to the real lead volume.
4. For the top leads, generate call cards with context and talking points.
5. Optionally draft follow-ups and propose calendar slots.

Rules:

- Never send follow-ups automatically.
- Never create calendar events without approval.
- Never contaminate the list with customers or unqualified contacts.

### Content strategy

Run when the owner asks:

- what should I post
- what is selling
- what should I promote
- content plan

Workflow:

1. Clarify the metric that matters most: revenue, margin, velocity, or a mix.
2. Pull 90-day sales data from QuickBooks, PayPal, or Square.
3. Identify top performers, slow movers, rising items, and fading items.
4. Layer in seasonality or known business context.
5. Produce a 30-day content brief with:
   - push hard
   - hold steady
   - reposition or pause
   - seasonal opportunities
   - recommended offers

Rules:

- Strategic output only at this stage.
- Keep the brief concise and actionable.
- Do not fabricate seasonality when neither data nor owner context supports it.

### Campaign execution

Run when the owner wants the strategy turned into real assets and staged posts.

Workflow:

1. Require an approved brief first.
2. Build a posting calendar and separate social vs text-only channels.
3. Inventory every Canva asset slot before generation.
4. Generate Canva-bound social assets one row at a time with quota-aware pacing.
5. Draft captions and plain-text email copy.
6. Stage social posts in HubSpot if supported.
7. Surface email content for manual sending.

Rules:

- Every stage requires owner approval.
- Never use Canva for email rows.
- Never publish directly; stage only.
- On quota errors, pause and ask how to proceed rather than retrying blindly.

### Sales brief

Run when the owner wants a faster readout on what is selling and what deserves marketing effort.

Workflow:

1. Pull recent sales performance.
2. Rank top and bottom sellers.
3. Pair the findings with concise promotion guidance or a follow-on content brief.

## Output Guidance

Use:

- ranked lead tables
- call cards
- 30-day content briefs
- posting calendars
- caption and email drafts
- staged-campaign summaries

## Guardrails

- No outbound sending without explicit owner approval.
- No hidden connector dependencies; explain what is missing.
- No asset generation before the calendar and slot inventory are approved.

