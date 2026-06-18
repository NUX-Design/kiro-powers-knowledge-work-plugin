# Setup and Routing

Use this workflow when an owner is new, asks "what can you do," needs setup help, or has an open-ended business request that should be routed to the right downstream workflow.

## Purpose

This steering file merges the source plugin’s `smb-onboard` and `smb-router` behaviors:

- onboarding and connector selection
- business-context capture
- weekly rhythm setup
- plain-English routing into the right operational workflow

## Onboarding Workflow

### 1. Assess the current state

- Check which connectors are already active.
- Check whether business context already exists.
- If returning, review what changed instead of re-interviewing from scratch.

### 2. Pick the first two functions to connect

Start from the owner’s main headaches:

- money or payroll
- customers or complaints
- sales or lead follow-up
- scheduling or getting organized

Describe connectors in terms of what Kiro will be able to do once connected, not what the platform itself is.

Rules:

- Connect one tool at a time.
- If the owner uses an unsupported tool, explain what becomes possible with the supported alternative and what remains blocked without it.
- Do not push a switch if the owner does not want one.

### 3. Prove value quickly

As soon as one relevant connector is available, run one small recipe that matches the owner’s biggest pain point:

- cash concern → finance snapshot
- customer concern → customer pulse or complaint handling
- sales concern → lead or campaign workflow

The goal is a fast "aha" moment, not a long setup flow.

### 4. Capture business context

Ask conversationally for:

- industry
- business size or stage
- top 3 headaches
- main tools already in use
- preferred weekly check-in cadence

Show the full profile before storing or updating it.

### 5. Set the weekly rhythm

Propose a recurring phrase and day, such as a Monday check-in. If the owner prefers another cadence, record that instead.

## Routing Workflow

When the owner makes an open-ended request, choose one best next workflow rather than dumping a menu.

### Routing Map

Money and finance:

- payroll concern, cash crunch, who owes me money → `cash-and-finance.md`
- month-end, reconcile, close the books → `cash-and-finance.md`
- margins, costs, pricing pressure → `cash-and-finance.md`
- estimated taxes, 1099s, accountant prep → `cash-and-finance.md`

Sales and marketing:

- who should I call, hot leads, pipeline → `sales-and-marketing.md`
- sales are down, run a campaign, need more customers → `sales-and-marketing.md`
- what is selling, what should I promote → `sales-and-marketing.md`

Customer operations:

- what are customers saying, complaints, reviews → `customer-operations.md`
- angry customer, refund request, draft a response → `customer-operations.md`
- clean up the CRM, log the call, stale deals → `customer-operations.md`

Contracts:

- review this contract, NDA, should I sign this → `contracts.md`

Hiring:

- help me hire, write a job post, interview guide, offer letter → `hiring.md`

Business visibility:

- monday brief, end-of-week recap, how is the business doing → `business-briefs.md`

### Connector-aware routing

Before recommending a route:

- Check whether required connectors exist.
- If a key connector is missing, say so up front.
- Offer onboarding or the nearest partial fallback when possible.
- Never silently route to a workflow that cannot do meaningful work.

### Recommendation style

Use:

- one recommendation
- one short reason
- one confirmation question

Do not dump a full command list unless the owner explicitly asks for a broad overview.

## Guardrails

- Never perform the downstream workflow inside the router itself; it should direct the user to the right path.
- Never overwrite stored business context without showing the proposed change first.
- Never connect tools on the owner’s behalf; guide only.

