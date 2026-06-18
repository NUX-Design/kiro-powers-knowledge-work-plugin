# Draft Offer

Use this workflow when a candidate is ready for an offer, when a hiring manager needs a clear compensation package, or when the team wants negotiation notes alongside the offer letter.

## Inputs

Gather:

- role and title
- level
- location
- base salary
- equity details
- signing bonus or target bonus if applicable
- start date
- hiring manager

If some details are missing, help the user identify what still needs a decision.

## Core Output

Produce:

- compensation-package summary
- key employment terms
- benefits highlights relevant to the candidate
- complete offer-letter draft text
- hiring-manager notes about negotiation, band context, or flags

## Connector-Aware Enhancements

If live systems exist:

- HRIS can provide band context and benefits defaults
- ATS can provide candidate details and pipeline status

If they do not exist, proceed entirely from manual inputs.

## Output Format

```markdown
## Offer Letter Draft: [Role] — [Level]

### Compensation Package
| Component | Details |
|---|---|
| Base Salary | [amount] |
| Equity | [grant and vesting] |
| Signing Bonus | [if any] |
| Target Bonus | [if any] |
| Total First-Year Comp | [amount] |

### Terms
- Start Date: [date]
- Reports To: [manager]
- Location: [location]
- Employment Type: [type]

### Benefits Summary
[summary]

### Offer Letter Text
[full draft]

### Notes for Hiring Manager
- [note]
```

## Guardrails

- Include total compensation, not just base.
- Be specific about equity mechanics where available.
- Keep the letter warm but clear.
- Do not invent compensation details the user has not provided.

