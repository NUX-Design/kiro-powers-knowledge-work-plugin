# Legal Response Templates

Use this workflow to draft a response to a common legal inquiry using configured templates or a fallback structure. Always perform escalation checks before producing a routine response.

Important: Drafts from this workflow should be reviewed before sending. Some categories require counsel review even when a template exists.

## Common Inquiry Types

- `dsr` or `data-subject-request`
- `hold` or `discovery-hold`
- `vendor` or `vendor-question`
- `nda` or `nda-request`
- `privacy` or `privacy-inquiry`
- `subpoena`
- `insurance`
- `custom`

If no type is specified, ask which category applies.

## Step 1: Load a Template

Look for local templates or user configuration.

If a template exists:

- Load it
- Identify required variables
- Confirm the output still fits the current facts

If no template exists:

- Say so
- Offer a fallback draft structure
- Offer to help create a reusable template

## Step 2: Escalation Check

Before drafting, check whether the matter should not use a routine template.

### Universal Escalation Triggers

- Litigation or regulatory investigation risk
- Government or law-enforcement sender
- Potential legal waiver or binding commitment
- Criminal exposure
- Likely media attention
- Novel or unprecedented situation
- Multiple jurisdictions with conflicting rules
- Executive or board involvement

### Category-Specific Triggers

Data subject requests:

- Minor’s data
- Litigation hold implications
- Active employee dispute
- Broad fishing-expedition scope
- Special-category data

Discovery holds:

- Criminal exposure
- Unclear or disputed scope
- Significant operational burden
- Conflict with deletion requirements

Vendor questions:

- Dispute or breach allegations
- Threatened termination or litigation
- Regulatory implications
- Commitment that may affect negotiations

NDA requests:

- Competitor counterparty
- Government-classified information
- Potential M&A context
- Unusual data categories

Subpoenas and legal process:

- Always require counsel review

### If a Trigger Fires

1. Stop routine generation.
2. Explain the trigger clearly.
3. Recommend the right escalation path.
4. If helpful, produce a clearly labeled draft for counsel review only.

## Step 3: Gather Details

Collect the variables needed for the category.

Examples:

- DSR: requester, request type, jurisdiction, deadline
- Hold notice: matter, custodians, scope, effective date, counsel contact
- Vendor question: vendor, agreement, issue, relevant provisions
- NDA request: business sponsor, counterparty, purpose, directionality

## Step 4: Draft the Response

Every draft must be customized with:

- Correct names
- Dates and deadlines
- Matter or request IDs
- Applicable law or jurisdiction
- Correct signature block

Adjust tone based on:

- Internal vs external audience
- Business vs legal audience
- Sensitivity level
- Urgency

## Response Structures

### Data Subject Requests

Key elements:

- Applicable law reference
- Deadline
- Identity verification if needed
- Rights information
- Contact for follow-up

### Discovery Holds

Key elements:

- Privileged heading where appropriate
- Clear preservation scope
- Effective date
- Acknowledgment requirement
- Contact for questions

### Vendor Questions

Key elements:

- Agreement reference
- Direct answer to the question
- Caveats and next steps

### NDA Requests

Key elements:

- Purpose
- Standard terms summary
- Execution or review process

### Subpoena / Legal Process

Use only as a starting framework for counsel-reviewed work.

### Insurance Notifications

Key elements:

- Policy info
- Incident or matter summary
- Timeline
- Requested coverage confirmation

## Template Creation Guidance

When building a reusable template, include:

- Category
- Use case
- Escalation triggers
- Required variables
- Subject line
- Body
- Follow-up actions
- Last reviewed date and approver

Suggested format:

```markdown
## Template: [Name]
**Category**: [category]
**Version**: [version]
**Last Reviewed**: [date]
**Approved By**: [approver]

### Use When
- [condition]

### Do Not Use When
- [trigger]

### Variables
| Variable | Description | Example |
|---|---|---|
| {{name}} | [meaning] | [example] |

### Subject Line
[subject]

### Body
[template body]

### Follow-Up Actions
1. [action]
2. [action]
```

## Output Format

```markdown
## Generated Response: [Inquiry Type]

**To**: [recipient]
**Subject**: [subject]

---

[response body]

---

### Escalation Check
[clear statement of whether triggers were found]

### Follow-Up Actions
1. [action]
2. [action]
3. [action]
```

## Final Rules

- Present drafts for review rather than assuming they should be sent.
- Surface deadlines explicitly for regulated responses.
- If email tools are connected, drafting can be suggested, but review still comes first.
- Treat templates as living documents and recommend updates when manual edits recur.

