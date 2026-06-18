# Contract Review Against Playbook

Use this workflow when reviewing a contract against your organization's negotiation playbook. The goal is to flag deviations, generate practical redlines, explain business impact, and frame a negotiation strategy.

Important: This workflow supports legal operations. It does not provide legal advice. Analysis should be reviewed by qualified legal professionals.

## Inputs

Accept the contract in any of these forms:

- File upload such as PDF or DOCX
- URL to a document or CLM record
- Pasted contract text

If no contract is provided, ask for one.

## Required Context

Before reviewing, gather:

1. Which side the user represents: vendor, customer, licensor, licensee, partner, or other.
2. Deadline or urgency.
3. Focus areas such as data protection, liability, IP, or termination.
4. Deal context such as strategic importance, value, or relationship history.

If context is incomplete, proceed with explicit assumptions.

## Load the Playbook

Look for a local legal playbook such as `legal.local.md` or equivalent user configuration.

The playbook should define:

- Standard positions
- Acceptable fallback ranges
- Escalation triggers

If no playbook is available:

- Say so clearly.
- Offer to help define one.
- Or proceed using general commercial standards as a fallback baseline.
- Mark the review basis as generic rather than organization-specific.

## Review Method

1. Identify the contract type.
2. Determine the user's side because that changes the analysis.
3. Read the whole contract before drawing conclusions.
4. Review each material clause against the playbook or fallback standards.
5. Assess the contract holistically, not as isolated clauses.

Cover at minimum:

| Clause Category | Review Focus |
|---|---|
| Limitation of liability | Cap, carveouts, mutuality, consequential damages |
| Indemnification | Scope, control of defense, caps, survival |
| IP ownership | Pre-existing IP, work product, assignment, licenses |
| Data protection | DPA, breach timing, subprocessors, transfers, deletion |
| Confidentiality | Scope, term, carveouts, handling requirements |
| Reps and warranties | Scope, disclaimers, survival |
| Term and termination | Renewal, convenience rights, cure periods, wind-down |
| Governing law and disputes | Jurisdiction, venue, arbitration, fees |
| Insurance | Coverage, minimums, evidence |
| Assignment | Consent rules and change-of-control treatment |
| Force majeure | Scope, notices, termination rights |
| Payment terms | Timing, taxes, late fees, increases |

## Clause Guidance

### Limitation of Liability

Check:

- Cap structure and amount
- Mutuality
- Carveouts that make the cap ineffective
- Consequential damage exclusions and exceptions
- Whether the cap is per-claim or aggregate

Typical problems:

- Cap tied to a very small fee period
- One-sided carveouts
- Broad carveouts swallowing the cap
- Missing mutual exclusion of indirect damages

### Indemnification

Check:

- Whether obligations are mutual or unilateral
- Triggering events such as IP, data breach, or bodily injury
- Relationship to the general liability cap
- Notice, defense, settlement, and mitigation mechanics

Typical problems:

- Indemnity for any breach
- No defense-control rights
- Unlimited survival

### Intellectual Property

Check:

- Ownership of pre-existing IP
- Ownership of created materials
- Work-for-hire scope
- License breadth and sublicensing
- Feedback clauses

Typical problems:

- Assignment language that captures pre-existing assets
- Work-for-hire clauses drafted too broadly
- Unbounded feedback licenses

### Data Protection

Check:

- Whether a DPA is required
- Roles of controller and processor
- Subprocessor approval and notice rules
- Breach notice timing
- Cross-border transfer safeguards
- Deletion, return, audit, and security terms

Typical problems:

- No DPA
- Blanket subprocessor rights
- Breach notice too slow to support regulatory deadlines
- Weak transfer protections

### Term and Termination

Check:

- Initial term and renewal mechanics
- Convenience termination rights
- Cure periods for breach
- Effects of termination including transition assistance
- Survival language

Typical problems:

- Long initial term with no convenience exit
- Auto-renewal with short notice windows
- No meaningful transition support

### Governing Law and Disputes

Check:

- Jurisdiction and venue
- Arbitration requirements and forum rules
- Jury waiver, class waiver, or fee-shifting provisions
- Pre-dispute escalation requirements

Typical problems:

- Unfavorable or remote forum
- Mandatory arbitration skewed toward the drafter
- Dispute process without escalation steps

## Classification Rules

Classify deviations with a three-tier system:

### GREEN

Use when the clause matches or improves on the standard position. Minor commercial variation is acceptable.

Action:

- Note it.
- No negotiation required.

### YELLOW

Use when the clause is outside the preferred position but still negotiable.

Action:

- Provide a specific redline.
- Include fallback language.
- Explain the business impact of accepting the clause.

### RED

Use when the clause triggers escalation or creates material exposure.

Action:

- Explain the specific risk.
- Provide a market-standard alternative.
- Estimate exposure where possible.
- Recommend escalation to senior or outside counsel as appropriate.

## Redline Format

For each YELLOW or RED issue, provide:

```markdown
**Clause**: [section and clause name]
**Current language**: "[relevant contract text]"
**Proposed redline**: "[specific alternative language]"
**Rationale**: [brief explanation suitable for external sharing]
**Priority**: [Must-have / Should-have / Nice-to-have]
**Fallback**: [backup position if needed]
```

Redlines should be specific, commercially reasonable, and prioritized. Avoid vague suggestions.

## Negotiation Strategy

Organize issues into:

- Tier 1: must-haves or deal breakers
- Tier 2: strong preferences with meaningful risk impact
- Tier 3: concession candidates

Lead with Tier 1 items. Use Tier 3 items strategically. Do not concede Tier 1 without escalation.

## Optional CLM Routing

If a CLM or approval system is connected, suggest the correct routing path based on risk, value, and contract type. If not connected, skip this cleanly.

## Output Format

```markdown
## Contract Review Summary

**Document**: [name]
**Parties**: [names]
**Your Side**: [role]
**Deadline**: [if known]
**Review Basis**: [Playbook / Generic Standards]

## Key Findings
[Top issues with GREEN / YELLOW / RED flags]

## Clause-by-Clause Analysis

### [Clause Category] - [GREEN / YELLOW / RED]
**Contract says**: [summary]
**Playbook position**: [standard position]
**Deviation**: [gap]
**Business impact**: [practical effect]
**Redline suggestion**: [if needed]

## Negotiation Strategy
[priorities and concessions]

## Next Steps
[specific follow-up actions]
```

## Notes

- If the contract is in another language, confirm whether review should proceed in the original language or with translation support.
- For very long agreements, offer a material-issues-first pass followed by full review.
- Always restate that the output should be reviewed by qualified counsel before use.

