# Cash and Finance

Use this workflow for payroll confidence, cash forecasting, overdue invoices, pricing pressure, month-end close, and accountant-facing tax prep.

This steering file merges the source plugin’s:

- `cash-flow-snapshot`
- `invoice-chase`
- `margin-analyzer`
- `month-end-prep`
- `tax-season-organizer`
- plus orchestration wrappers such as `plan-payroll`, `month-heads-up`, `close-month`, `price-check`, and `tax-prep`

## Finance Modes

### Payroll and cash confidence

Run when the owner asks:

- can I make payroll
- cash is tight
- what does next month look like
- runway

Workflow:

1. Pull cash position, receivables, payables, and fixed costs.
2. Compute 30/60/90-day net cash outlook with confidence bands where data supports it.
3. Flag named risks such as late payers, payroll crunches, or thin-data warnings.
4. If needed, rank overdue invoices and draft reminders.
5. Stage reminders only after explicit owner approval.

Rules:

- Forecast first, then collections.
- Never send reminders without approval.
- If the forecast shows payroll is clearly covered, ask whether chasing invoices is still worthwhile.

### Overdue invoice chase

Run when the owner wants to know who owes money or wants reminders drafted.

Workflow:

1. Pull overdue receivables from QuickBooks and optionally Stripe.
2. Cross-reference recent payment history from PayPal where available.
3. Score each customer as good payer, occasionally late, or repeat late.
4. Draft one consolidated reminder per customer.
5. Present a summary table and the full drafts.
6. Send or queue only after owner approval.

Rules:

- Exclude customers who appear recently paid; mark them as verify-first.
- Do not fabricate contact or invoice context.
- One batch approval covers only the presented batch.

### Margin and pricing analysis

Run when the owner asks what to charge, whether costs are rising, or whether margins are healthy.

Workflow:

1. Clarify which products or services are in scope.
2. Pull cost data from QuickBooks and revenue data from PayPal or Square.
3. Compute revenue, COGS, gross profit, gross margin, and per-unit economics.
4. Layer in inflation, seasonality, and industry benchmarks when possible.
5. Model pricing scenarios at multiple uplift levels.
6. Present the data without making the final pricing decision for the owner.

Rules:

- Surface data, not prescriptive pricing advice.
- If COGS are missing, stop and request a rough cost breakdown.
- State assumptions clearly for any elasticity or benchmark math.

### Month-end close

Run when the owner wants to reconcile the month and produce a close packet.

Workflow:

1. Confirm the target month and verify the books are still open.
2. Pull QuickBooks P&L and transaction register.
3. Pull payment-processor settlements for the same period.
4. Match deposits and flag discrepancies, uncategorized transactions, duplicates, and missing receipts.
5. Pause for owner triage before generating the narrative or export packet.
6. Write a plain-English P&L summary.
7. Export a close packet workbook and summary file.

Rules:

- Never auto-fix QuickBooks entries.
- Never delete suspected duplicates automatically.
- Always pause before final export if material gaps remain unresolved.

### Tax prep for the accountant

Run in two major modes:

- quarterly estimated-tax prep
- year-end 1099 prep

Quarterly estimate workflow:

1. Pull year-to-date P&L.
2. Ask about estimated payments already made.
3. Estimate self-employment tax and federal income tax using explicit assumptions.
4. Compute a quarterly payment view and due date.
5. Deliver a structured summary marked for accountant review.

1099-prep workflow:

1. Pull contractor and vendor payments from QuickBooks and processors.
2. Aggregate by payee.
3. Apply threshold logic.
4. Flag W-9 status and likely duplicates.
5. Deliver a candidate list plus missing-W-9 action items.

Rules:

- Frame the output as prep material for a CPA, not tax advice.
- State every assumption.
- Do not file anything.
- Do not auto-merge ambiguous payees.

## Output Guidance

Use concise, owner-readable structures such as:

- forecast summary tables
- overdue-invoice summary tables
- unit-economics tables
- reconciliation gap lists
- accountant-facing tax summaries

Always name actual records, customers, amounts, and due dates when available.

## Guardrails

- No money-touching action without explicit approval.
- No legal or tax advice framing.
- No invented numbers or missing-source assumptions.
- If a connector is missing, either degrade explicitly or stop when it is a true hard dependency.

