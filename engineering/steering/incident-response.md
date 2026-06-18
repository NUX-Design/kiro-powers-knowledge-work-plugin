# Incident Response

Manage an incident from detection through postmortem.

## Modes

- `new`: start a new incident and assess severity
- `update`: produce a status update for the current incident state
- `postmortem`: generate a blameless postmortem after resolution

If no mode is clear, determine which phase the incident is in first.

## Workflow

```text
┌─────────────────────────────────────────────────────────────────┐
│                      INCIDENT RESPONSE                          │
├─────────────────────────────────────────────────────────────────┤
│  Phase 1: TRIAGE                                                │
│  ✓ Assess severity (SEV1-4)                                     │
│  ✓ Identify affected systems and users                          │
│  ✓ Assign roles                                                 │
│                                                                 │
│  Phase 2: COMMUNICATE                                           │
│  ✓ Draft internal and external updates                          │
│  ✓ Set update cadence                                           │
│                                                                 │
│  Phase 3: MITIGATE                                              │
│  ✓ Track mitigation steps                                       │
│  ✓ Maintain a timeline                                          │
│  ✓ Confirm resolution                                           │
│                                                                 │
│  Phase 4: POSTMORTEM                                            │
│  ✓ Reconstruct the timeline                                     │
│  ✓ Perform root-cause analysis                                  │
│  ✓ Create follow-up actions                                     │
└─────────────────────────────────────────────────────────────────┘
```

## Severity Guide

| Level | Criteria | Response Time |
|-------|----------|---------------|
| SEV1 | Service down, all users affected | Immediate, all-hands |
| SEV2 | Major feature degraded, many users affected | Within 15 min |
| SEV3 | Minor feature issue, some users affected | Within 1 hour |
| SEV4 | Cosmetic or low-impact issue | Next business day |

## Communication Guidance

Keep updates factual and regular. Always include what is happening, who is affected, what actions are underway, and when the next update will arrive.

## Output: Status Update

```markdown
## Incident Update: [Title]
**Severity:** SEV[1-4] | **Status:** Investigating | Identified | Monitoring | Resolved
**Impact:** [Who/what is affected]
**Last Updated:** [Timestamp]

### Current Status
[What we know now]

### Actions Taken
- [Action 1]
- [Action 2]

### Next Steps
- [What's happening next and ETA]

### Timeline
| Time | Event |
|------|-------|
| [HH:MM] | [Event] |
```

## Output: Postmortem

```markdown
## Postmortem: [Incident Title]
**Date:** [Date] | **Duration:** [X hours] | **Severity:** SEV[X]
**Authors:** [Names] | **Status:** Draft

### Summary
[2-3 sentence plain-language summary]

### Impact
- [Users affected]
- [Duration of impact]
- [Business impact if quantifiable]

### Timeline
| Time (UTC) | Event |
|------------|-------|
| [HH:MM] | [Event] |

### Root Cause
[Detailed explanation of what caused the incident]

### 5 Whys
1. Why did [symptom]? → [Because...]
2. Why did [cause 1]? → [Because...]
3. Why did [cause 2]? → [Because...]
4. Why did [cause 3]? → [Because...]
5. Why did [cause 4]? → [Root cause]

### What Went Well
- [Things that worked]

### What Went Poorly
- [Things that didn't work]

### Action Items
| Action | Owner | Priority | Due Date |
|--------|-------|----------|----------|
| [Action] | [Person] | P0/P1/P2 | [Date] |

### Lessons Learned
[Key takeaways for the team]
```

## If Relevant MCP Tools Are Connected

- Pull alerts and metrics from monitoring tools.
- Update incident records or page responders through incident tooling.
- Post updates to chat channels automatically.

## Tips

1. Start documenting before you know everything.
2. Separate facts from hypotheses.
3. Keep postmortems blameless and system-focused.
