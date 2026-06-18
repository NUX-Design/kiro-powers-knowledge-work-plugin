# NDA Triage

Use this workflow to screen an incoming NDA quickly and classify it as GREEN, YELLOW, or RED for routing.

Important: This workflow supports legal operations. It does not provide legal advice. Counsel should review uncertainty or escalated issues.

## Inputs

Accept:

- File uploads
- URLs
- Pasted NDA text

If nothing is provided, ask for the NDA first.

## Load the NDA Playbook

Look for local configuration such as `legal.local.md`.

If no NDA-specific playbook exists, use fallback defaults:

- Mutual obligations required unless a one-way disclosure context clearly justifies unilateral form
- Standard term of 2 to 3 years, with up to 5 years for trade secrets
- Standard carveouts: public, prior possession, independent development, third-party receipt, legal compulsion
- No non-solicit or non-compete
- No broad residuals clause
- Reasonable commercial governing law

State clearly when defaults are being used.

## Screening Checklist

### Agreement Structure

- Identify whether it is mutual or unilateral.
- Check whether that structure fits the business context.
- Confirm it is a real NDA rather than a broader commercial agreement.

### Definition of Confidential Information

- Scope should be reasonable.
- Marking requirements should be workable.
- Standard exclusions should be present.
- Public or independently developed information should not be swept in.

### Receiving-Party Obligations

- Standard of care should be reasonable.
- Use restrictions should tie to the stated purpose.
- Disclosure restrictions should permit need-to-know sharing.
- Practical burdens should not be excessive.

### Standard Carveouts

Verify:

- Public knowledge
- Prior possession
- Independent development
- Third-party lawful receipt
- Legal compulsion

### Permitted Disclosures

Check for:

- Employees
- Contractors and advisors
- Affiliates if needed
- Legal or regulatory disclosures

### Term and Duration

- Agreement term should be commercially reasonable.
- Confidentiality survival should be finite except where trade secret treatment justifies longer protection.

### Return and Destruction

- Trigger should be on request or termination.
- Retention exceptions for law, backup, or compliance should exist.
- Certification of destruction should be reasonable.

### Remedies

- Injunctive relief language is normal.
- Liquidated damages are a red flag.
- Remedies should not be one-sided in a mutual NDA.

### Problematic Provisions

Flag:

- Non-solicit
- Non-compete
- Exclusivity
- Standstill
- Broad residuals clause
- IP assignment or license
- Audit rights

### Governing Law and Jurisdiction

- Use a reasonable commercial forum.
- Avoid highly unfavorable jurisdiction or mandatory arbitration in standard NDA scenarios.

## Classification

### GREEN

Use when the NDA is effectively standard:

- Correct structure
- Standard carveouts present
- Reasonable term
- No major restrictive extras
- Reasonable governing law

Action: approve via standard delegation.

### YELLOW

Use when issues exist but are narrow and likely resolvable in one review pass:

- Slightly broad definition
- Longer but still market-range term
- Missing a non-critical carveout
- Narrow residuals language
- Acceptable but non-preferred forum
- Minor asymmetry

Action: send for counsel review with issues flagged.

### RED

Use when significant issues exist:

- Wrong agreement direction
- Missing critical carveouts
- Non-solicit, non-compete, exclusivity, or standstill
- Very long or perpetual term without justification
- Overbroad definition
- Broad residuals clause
- Hidden IP license or assignment
- Liquidated damages
- Highly unfavorable forum
- The document is not actually just an NDA

Action: do not approve; escalate for full review or counter with standard form.

## Report Format

```markdown
## NDA Triage Report

**Classification**: [GREEN / YELLOW / RED]
**Parties**: [names]
**Type**: [Mutual / Unilateral]
**Term**: [duration]
**Governing Law**: [jurisdiction]
**Review Basis**: [Playbook / Default Standards]

## Screening Results

| Criterion | Status | Notes |
|---|---|---|
| Mutual Obligations | PASS / FLAG / FAIL | [details] |
| Definition Scope | PASS / FLAG / FAIL | [details] |
| Standard Carveouts | PASS / FLAG / FAIL | [details] |
| Term | PASS / FLAG / FAIL | [details] |

## Issues Found

### [Issue - YELLOW or RED]
**What**: [issue]
**Risk**: [practical risk]
**Suggested Fix**: [language or approach]

## Recommendation
[approve / review / reject or counter]

## Next Steps
1. [action]
2. [action]
```

## Common Issue Guidance

- Overbroad confidentiality definition: narrow to genuinely non-public information and reasonable confidentiality expectations.
- Missing independent-development carveout: add it because otherwise internal development may be chilled.
- Non-solicit in an NDA: remove it unless a separate business context clearly justifies it.
- Broad residuals clause: resist or limit to unaided memory and exclude trade secrets and patentable information.
- Perpetual confidentiality: replace with a defined term, with trade secret treatment carved out if needed.

## Routing Guidance

| Classification | Action | Typical Timeline |
|---|---|---|
| GREEN | Approve and route for signature | Same day |
| YELLOW | Send to designated reviewer with notes | 1 to 2 business days |
| RED | Full review and likely counterproposal | 3 to 5 business days |

