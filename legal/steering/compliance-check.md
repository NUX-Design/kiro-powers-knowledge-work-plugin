# Compliance Check

Use this workflow to assess a proposed product feature, campaign, business initiative, or operational change for compliance exposure.

Important: Regulatory requirements change frequently. This workflow is a structured screening aid, not legal advice.

## Input

Ask the user to describe the initiative with as much specificity as possible, including:

- What they want to do
- Geography or jurisdictions involved
- Types of personal or sensitive data involved
- Target users or customers
- Timing and launch pressure

## Output Format

```markdown
## Compliance Check: [Initiative]

### Summary
[Proceed / Proceed with conditions / Requires further review]

### Applicable Regulations and Policies
| Regulation/Policy | Relevance | Key Requirements |
|---|---|---|
| [law or policy] | [why it matters] | [what must be done] |

### Requirements
| # | Requirement | Status | Action Needed |
|---|---|---|---|
| 1 | [requirement] | Met / Not Met / Unknown | [action] |

### Risk Areas
| Risk | Severity | Mitigation |
|---|---|---|
| [risk] | High / Med / Low | [mitigation] |

### Recommended Actions
1. [action]
2. [action]
3. [action]

### Approvals Needed
| Approver | Why | Status |
|---|---|---|
| [team or role] | [reason] | Pending |

### Further Review Recommended
[specialist or outside-counsel review areas]
```

## Core Review Areas

### Privacy and Data Protection

Assess:

- Lawful basis for processing
- Consent requirements
- Privacy notices
- Data minimization
- Retention limits
- Data subject rights handling
- Security controls
- International transfers

### Product and Marketing

Assess:

- Claims substantiation
- Use of testimonials or endorsements
- Referral incentives
- Children or minors exposure
- Tracking, cookies, or profiling
- Automated decision-making concerns

### Vendor and Operational Dependencies

Assess:

- Need for DPAs
- Vendor subprocessors
- Data location
- Security certification expectations
- Contractual restrictions

## Regulatory Reference Points

### GDPR

Check for:

- EU or EEA data subject scope
- Lawful basis
- DPIA needs
- 72-hour breach notification implications
- Article 30 recordkeeping
- Transfer mechanisms
- DPO implications

### CCPA / CPRA

Check for:

- Threshold applicability
- Notice-at-collection obligations
- Access, deletion, correction, and opt-out rights
- Sensitive personal information handling
- Service-provider contract terms

### Other Jurisdictions

Depending on the facts, consider laws such as LGPD, POPIA, PIPEDA, PDPA, the Australian Privacy Act, PIPL, and UK GDPR. Do not assume one regime is sufficient if the initiative is cross-border.

## DPA Review Checklist

When the initiative depends on a vendor processing personal data, verify:

- Subject matter and duration are defined
- Nature and purpose are clear
- Data types and subject categories are listed
- Processor acts only on instructions
- Confidentiality and security commitments exist
- Subprocessor controls exist
- Assistance with rights requests, breaches, DPIAs, and audits exists
- Deletion or return on termination is covered
- Transfer mechanisms are valid and current

Common problems:

- Blanket subprocessor approval without notice
- Breach notice timing too slow
- Missing audit rights
- Undefined deletion timing
- Unspecified processing locations
- Outdated SCC language

## Data Subject Requests

When the scenario includes DSR handling, verify:

- Request type
- Applicable law
- Identity verification
- Logging and deadlines
- Potential exemptions such as legal hold or mandatory retention
- Response process and documentation

## Monitoring and Escalation

Escalate when:

- A new rule directly affects the business model
- A regulator is involved
- Enforcement activity signals heightened scrutiny in the company’s sector
- A compliance deadline requires organizational change
- Cross-border transfer mechanics are uncertain or challenged

## Practical Guidance

1. Be concrete. "EU customer analytics using biometrics" is far more useful than "new feature."
2. Include data categories and geographies early.
3. Mark unknowns explicitly rather than guessing.
4. Separate legal requirements from internal policy requirements.

