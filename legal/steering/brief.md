# Legal Briefing

Use this workflow to generate legal briefings in one of three modes:

- Daily brief
- Topic brief
- Incident brief

Important: These briefings organize available information. They do not replace legal advice or formal legal research.

## Mode Selection

If the user does not specify a mode, ask whether they need:

- `daily`
- `topic <query>`
- `incident <topic>`

## Daily Brief

Build a concise morning scan of legal-relevant work.

### Sources to Check

If connected, review:

- Email for contract requests, compliance questions, counterparty responses, external counsel updates, and urgent inbox items
- Calendar for meetings needing legal preparation and deadlines this week
- Chat for overnight legal requests, escalations, and topic mentions
- CLM for contracts awaiting review, signature, or renewal
- CRM for deals reaching stages that need legal involvement

### Output

```markdown
## Daily Legal Brief - [Date]

### Urgent / Action Required
[items]

### Contract Pipeline
- Awaiting review: [items]
- Pending counterparty response: [items]
- Approaching deadlines: [items]

### New Requests
[items]

### Calendar Today
[meetings and prep needs]

### Team Activity
[key messages or updates]

### This Week's Deadlines
[deadlines]

### Sources Not Available
[gaps]
```

## Topic Brief

Use for internal research on a legal question.

### Workflow

1. Accept the topic.
2. Search connected documents, email, chat, and contract systems for internal precedent.
3. Synthesize findings without overstating certainty.

### Output

```markdown
## Topic Brief: [Topic]

### Summary
[2 to 3 sentences]

### Background
[context from available materials]

### Current State
[current internal position or pattern]

### Key Considerations
[risks, tradeoffs, open questions]

### Internal Precedent
[prior decisions or materials]

### Gaps
[missing information]

### Recommended Next Steps
[what to do next]
```

If the topic needs current law or case authority, recommend formal legal research tools or counsel.

## Incident Brief

Use for fast response to a developing issue such as a data breach, dispute, investigation, or IP problem.

### Workflow

1. Accept the incident topic or description.
2. Search connected email, chat, docs, calendar, and contract systems for immediate context.
3. Produce a practical brief quickly with explicit gaps.

### Output

```markdown
## Incident Brief: [Topic]
**Prepared**: [timestamp]
**Classification**: [severity if determinable]

### Situation Summary
[what is known]

### Timeline
[ordered events]

### Immediate Legal Considerations
[notification, preservation, privilege, contractual duties]

### Relevant Agreements
[contracts, insurance, indemnities, DPAs]

### Internal Response
[what has already happened]

### Key Contacts
[important people]

### Recommended Immediate Actions
1. [action]
2. [action]
3. [action]

### Information Gaps
[unknowns]

### Sources Checked
[systems searched and systems unavailable]
```

## General Rules

- Keep briefs actionable and concise.
- Highlight missing systems or unverified facts prominently.
- Prefer linking to source materials over restating them in full.
- For incident work, flag litigation hold, preservation, notification, and outside-counsel considerations early.

