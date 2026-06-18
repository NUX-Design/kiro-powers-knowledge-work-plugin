# Architecture Decision Records

Create an Architecture Decision Record or evaluate a proposed system design.

## Common Modes

- Create an ADR for a technology or topology choice.
- Evaluate an existing design proposal.
- Design a new component or service from requirements and constraints.

For deeper system decomposition, pair this with `system-design.md`.

## Output Format

```markdown
# ADR-[number]: [Title]

**Status:** Proposed | Accepted | Deprecated | Superseded
**Date:** [Date]
**Deciders:** [Who needs to sign off]

## Context
[What is the situation? What forces are at play?]

## Decision
[What is the change we're proposing?]

## Options Considered

### Option A: [Name]
| Dimension | Assessment |
|-----------|------------|
| Complexity | [Low/Med/High] |
| Cost | [Assessment] |
| Scalability | [Assessment] |
| Team familiarity | [Assessment] |

**Pros:** [List]
**Cons:** [List]

### Option B: [Name]
[Same format]

## Trade-off Analysis
[Key trade-offs between options with clear reasoning]

## Consequences
- [What becomes easier]
- [What becomes harder]
- [What will need revisiting]

## Action Items
1. [ ] [Implementation step]
2. [ ] [Follow-up]
```

## If Relevant MCP Tools Are Connected

- Search prior ADRs and design docs in a knowledge base.
- Link related epics and implementation tasks in a project tracker.

## Tips

1. State hard constraints upfront, including deadlines, traffic, compliance, and cost.
2. Name realistic alternatives even if one option seems obvious.
3. Include non-functional requirements alongside feature needs.
