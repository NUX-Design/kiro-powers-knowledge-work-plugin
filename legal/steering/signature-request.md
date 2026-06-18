# Signature Request

Use this workflow when a document is finalized and ready to route for signature.

Important: Verify that the document is in final form before setting up execution.

## Input

Accept:

- File upload
- URL to the final document
- Clear reference to the document under discussion

## Pre-Signature Checklist

Confirm:

- Document is final and free of unresolved redlines
- All exhibits and schedules are attached
- Legal entity names are correct
- Dates are correct or intentionally blank
- Signature blocks match authorized signers
- Required internal approvals are complete
- Appropriate counsel review has occurred

## Signing Setup

Gather:

- Signer names, emails, and titles
- Signing order: sequential or parallel
- Any internal approval before external signature
- CC recipients for the executed copy

## Routing Logic

If an e-signature tool is connected:

- Create the envelope or request
- Set fields and order
- Add initial or date fields if required
- Send for signature

If no such tool is connected:

- Produce signing instructions
- List signers and order clearly
- Note expected manual next steps

## Output Format

```markdown
## Signature Request: [Document Title]

### Document Details
- **Type**: [MSA / NDA / SOW / Amendment / etc.]
- **Parties**: [Party A] and [Party B]
- **Pages**: [count]

### Pre-Signature Check: [PASS / ISSUES FOUND]
[issues if any]

### Signing Configuration
| Order | Signer | Email | Role |
|---|---|---|---|
| 1 | [name] | [email] | [role] |

### CC Recipients
- [name] - [email]

### Status
[Sent for signature / Ready to send / Issues to resolve first]

### Next Steps
- [action]
- [action]
- [action]
```

## Practical Reminders

1. Entity-name errors are common and costly.
2. Verify signatory authority before sending.
3. Ensure executed copies are filed in the right repository after completion.

