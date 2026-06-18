# Customer Operations

Use this workflow for customer sentiment synthesis, complaint handling, refunds, and HubSpot hygiene.

This steering file merges the source plugin’s:

- `customer-pulse`
- `ticket-deflector`
- `crm-maintenance`
- plus orchestration wrappers such as `customer-pulse-check`, `handle-complaint`, `crm-cleanup`, and related customer-facing flows

## Modes

### Customer pulse and feedback themes

Run when the owner asks:

- what are customers saying
- complaints
- reviews
- how are customers feeling

Workflow:

1. Pull signals from connected sources such as disputes, tickets, Gmail, Intercom, and pasted reviews.
2. Group them into 3 to 5 recurring themes.
3. Include verbatim evidence where available.
4. Rank the top fixable issues.
5. Produce a short "do these three things this week" list.
6. Optionally draft response templates tied to the top issues.

Rules:

- Degrade gracefully across sources.
- Do not include unnecessary customer PII in summary views.
- If a source is rate-limited or unavailable, note it and continue.

### Complaint handling and refund support

Run when the owner forwards an angry email, refund request, or customer complaint.

Workflow:

1. Read the customer message and extract the issue.
2. Pull order, payment, or refund status from payment systems.
3. Pull customer history from HubSpot where available.
4. Draft a tone-matched response in the owner’s voice.
5. If a refund appears warranted, surface a dedicated approval prompt with amount, customer, and transaction details.
6. Send or stage the response only after owner approval.
7. Log the interaction in HubSpot after the response path is settled.

Rules:

- Never issue a refund without explicit owner confirmation.
- Never send the response without owner review.
- Never fabricate order status or choose among ambiguous matches silently.

### CRM maintenance and cleanup

Run when the owner wants to:

- log an email
- log a call
- update a deal
- clean up stale HubSpot records

Workflow:

1. Identify whether the request is email logging, call logging, or cleanup.
2. Pull the relevant email, meeting, or deal context.
3. Resolve the right contact and deal in HubSpot.
4. Write the activity or prepare a cleanup diff.
5. For cleanup edits, present side-by-side current vs proposed values before any write.

Rules:

- Never delete records.
- Never create a new deal unprompted.
- Never change stage or close date without explicit approval.
- Announce contact creation before doing it.

## Output Guidance

Prefer:

- themed feedback summaries
- actionable fix lists
- drafted customer responses
- CRM activity confirmations
- current vs proposed cleanup diffs

## Guardrails

- No customer-facing send without approval.
- No refunds without approval.
- No silent record mutations in HubSpot.

