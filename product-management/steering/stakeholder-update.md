# Stakeholder Update

Use this workflow to generate an update tailored to a specific audience and cadence.

## Inputs

Identify:

- Update type: weekly, monthly, launch, or ad hoc
- Audience: executives, engineering, cross-functional partners, customers, or board

Pull context from trackers, chat, meeting notes, or docs when available. Otherwise ask for:

- What shipped or progressed
- Current blockers or risks
- Decisions made or needed
- What is next

## Audience Rules

### Executives

Optimize for:

- Outcome framing
- Status color
- Top progress
- Risks with mitigation
- Concrete asks

Keep it brief.

### Engineering

Optimize for:

- What shipped
- What is in progress
- Blockers
- Decisions
- Priority changes

### Cross-Functional Partners

Optimize for:

- What is coming that affects them
- What you need from them
- Timing and dependencies

### Customers

Optimize for:

- Benefits
- Clear timelines
- Known issues with workarounds
- Feedback channels

## Status Framework

- `Green`: on track
- `Yellow`: at risk
- `Red`: off track

Use real status, not optimistic status.

## Risk Communication

For each important risk, state:

- The risk
- Likely impact
- Confidence or likelihood
- Mitigation
- The ask, if any

## Output Templates

### Executive Update

```markdown
Status: [Green / Yellow / Red]

TL;DR: [one sentence]

Progress:
- [outcome]

Risks:
- [risk]: [mitigation]. [ask if needed]

Decisions Needed:
- [decision] - Need by [date]

Next Milestones:
- [milestone] - [date]
```

### Engineering Update

```markdown
Shipped:
- [item]

In Progress:
- [item] - [owner]

Decisions:
- [decision or question]

Priority Changes:
- [change]

Coming Up:
- [next item]
```

### Cross-Functional Update

```markdown
What's Coming:
- [item]

What We Need From You:
- [ask] by [date]

Decisions Made:
- [decision]

Open for Input:
- [topic]
```

### Customer Update

```markdown
What's New:
- [feature] - [benefit]

Coming Soon:
- [feature] - [timing]

Known Issues:
- [issue] - [workaround]

Feedback:
- [channel]
```

## Final Rules

- Lead with the most important thing.
- Match detail to audience attention span.
- Make asks specific and actionable.
- If there is bad news, surface it early.

