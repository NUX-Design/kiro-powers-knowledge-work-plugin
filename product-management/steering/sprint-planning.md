# Sprint Planning

Use this workflow to scope a sprint around real team capacity, clear priorities, and explicit risks.

## Inputs

Gather:

- Team members and availability
- Sprint length
- Prioritized backlog
- Carryover from the last sprint
- Dependencies or blockers

If a tracker or calendar is connected, use it to pull backlog and capacity constraints.

## Planning Rules

- Plan to roughly 70 to 80 percent of real capacity.
- Define one clear sprint goal.
- Identify stretch items explicitly.
- Treat carryover honestly and understand why it slipped.

## Workflow

1. Estimate capacity after PTO, meetings, on-call, and overhead.
2. Review carryover and whether it still deserves priority.
3. Sort backlog into must-ship, should-ship, and stretch.
4. Assign tentative owners.
5. Flag dependencies and risks.
6. Check total sprint load against realistic capacity.

## Output Format

```markdown
## Sprint Plan: [Sprint Name]
**Dates:** [start] - [end]
**Sprint Goal:** [one sentence]

### Capacity
| Person | Available Days | Allocation | Notes |
|---|---|---|---|
| [name] | [days] | [points or hours] | [PTO, on-call] |
| **Total** | **[days]** | **[points]** | |

### Sprint Backlog
| Priority | Item | Estimate | Owner | Dependencies |
|---|---|---|---|---|
| P0 | [item] | [estimate] | [owner] | [dependency] |

### Planned Capacity
[points planned] of [points available]

### Risks
| Risk | Impact | Mitigation |
|---|---|---|
| [risk] | [impact] | [mitigation] |

### Definition of Done
- [criterion]

### Key Dates
| Date | Event |
|---|---|
| [date] | [event] |
```

