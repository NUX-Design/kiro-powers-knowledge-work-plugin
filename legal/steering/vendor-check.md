# Vendor Check

Use this workflow to build a consolidated agreement-status report for a vendor across available systems.

Important: Treat the report as an operational summary that still needs confirmation against the underlying executed documents.

## Step 1: Identify the Vendor

Accept the vendor name and normalize common variations:

- Legal name vs trade name
- Parent vs subsidiary
- Common abbreviations

If ambiguous, ask the user to clarify the entity or group scope.

## Step 2: Search Available Systems

Check connected systems in priority order:

- CLM for active, expired, pending, and amended agreements
- CRM for account context and contacts
- Email for negotiation threads and attachments
- Document storage for executed agreements, drafts, and diligence material
- Chat for recent discussions and ad hoc requests

## Step 3: Summarize Each Agreement

Capture:

| Field | Details |
|---|---|
| Agreement Type | NDA, MSA, SOW, DPA, SLA, license, etc. |
| Status | Active, Expired, In Negotiation, Pending Signature |
| Effective Date | Start date |
| Expiration Date | End date or renewal timing |
| Auto-Renewal | Whether it renews and on what notice |
| Key Terms | Liability, law, termination, or other material points |
| Amendments | Any amendments or addenda |

## Step 4: Run Gap Analysis

Assess whether the relationship appears to need agreements such as:

- NDA
- MSA
- DPA
- SOW
- SLA
- Insurance certificate

Flag gaps based on the relationship. Example: if the vendor handles personal data and no DPA is found, call that out explicitly.

## Output Format

```markdown
## Vendor Agreement Status: [Vendor Name]

**Search Date**: [date]
**Sources Checked**: [systems]
**Sources Unavailable**: [systems]

## Relationship Overview

**Vendor**: [full name]
**Relationship Type**: [vendor / partner / customer / other]
**CRM Status**: [if available]

## Agreement Summary

### [Agreement Type] - [Status]
- **Effective**: [date]
- **Expires**: [date]
- **Auto-Renewal**: [details]
- **Key Terms**: [summary]
- **Location**: [where the file lives]

## Gap Analysis
[what exists, what may be missing]

## Upcoming Actions
- [renewals, expirations, missing docs, amendments]

## Notes
[relevant email or chat context]
```

## Missing-Source Handling

If systems are unavailable:

- Say exactly which ones were not checked.
- Suggest the manual fallback search path where useful.
- Do not imply the report is complete if core sources such as CLM or document storage were unavailable.

## Additional Notes

- If nothing is found anywhere, report that directly and ask whether agreements are stored elsewhere.
- Highlight agreements expiring within 90 days.
- Flag surviving obligations on expired agreements where relevant.

