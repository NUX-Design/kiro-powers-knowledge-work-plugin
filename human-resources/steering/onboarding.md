# Onboarding

Use this workflow to generate a pre-start checklist, Day 1 agenda, Week 1 plan, and 30/60/90 goals for a new hire.

## Inputs

Gather:

- new hire name
- role
- team
- start date
- manager

## Core Output

Include:

- pre-start checklist
- Day 1 schedule
- Week 1 priorities
- 30-day goals
- 60-day goals
- 90-day goals
- key contacts
- tools-access list

## Connector-Aware Enhancements

If available:

- HRIS can supply org-chart and team context
- knowledge-base tools can surface relevant onboarding docs
- calendar tools can support Day 1 and Week 1 scheduling

Without those, build the plan from the role and team context the user provides.

## Output Format

```markdown
## Onboarding Plan: [Name] — [Role]
**Start Date:** [date] | **Team:** [team] | **Manager:** [manager]

### Pre-Start
- [task]

### Day 1
| Time | Activity | With |
|---|---|---|
| [time] | [activity] | [owner] |

### Week 1
- [task]

### 30-Day Goals
1. [goal]

### 60-Day Goals
1. [goal]

### 90-Day Goals
1. [goal]

### Key Contacts
| Person | Role | For What |
|---|---|---|
| [name] | [role] | [purpose] |

### Tools Access Needed
| Tool | Access Level | Requested |
|---|---|---|
| [tool] | [level] | [status] |
```

## Guardrails

- Customize by role; avoid generic checklists if the role context supports better specificity.
- Do not overload Day 1.
- Include a buddy or equivalent support contact where possible.

