# Roadmap Update

Use this workflow to create, update, or reprioritize a roadmap.

## Inputs

Accept:

- Existing roadmap pasted or uploaded
- Description of current priorities
- A specific change request

If a project tracker is connected, pull the current roadmap state first.

## Determine the Operation

Identify whether the user wants to:

- Add an item
- Update status
- Reprioritize items
- Move timeline
- Create a new roadmap from scratch

## Core Information to Gather

- Item names and descriptions
- Priority
- Effort or capacity impact
- Owner
- Target timeframe
- Dependencies
- What changed, if this is a reprioritization

## Roadmap Summary Should Include

- Status overview
- Roadmap items
- Risks and dependencies
- Changes since last update

Group by:

- Now / Next / Later
- Quarter
- Theme
- OKR

Choose the format that best matches the user’s context.

## Roadmap Frameworks

### Now / Next / Later

- `Now`: committed work
- `Next`: planned work
- `Later`: directional work

Use when avoiding false precision matters.

### Quarterly Themes

Use when the roadmap needs strategic framing, not just sequencing.

### OKR-Aligned

Map items directly to objectives and key results.

### Timeline / Gantt View

Use when sequencing, dependencies, and scheduling detail matter.

## Prioritization Frameworks

Use when reprioritizing:

- RICE
- MoSCoW
- ICE
- Value vs effort

Show before-and-after priority changes when helpful.

## Dependency Management

Look for:

- Technical dependencies
- Team dependencies
- External dependencies
- Research dependencies
- Sequential dependencies

For each dependency, capture:

- Owner
- Need-by date
- Risk
- Contingency if it slips

## Capacity Rules

- Roadmaps are constrained by team capacity.
- When adding work, ask what moves or comes off.
- Surface overcommitment directly rather than hiding it.

## Communication Rules

When the roadmap changes:

1. State what changed.
2. Explain why.
3. Show the tradeoff.
4. Show the new plan.
5. Acknowledge who is affected.

## Output Format

```markdown
## Roadmap Update

### Status Overview
- [summary]

### Roadmap
| Bucket | Item | Status | Owner | Timeframe | Dependencies |
|---|---|---|---|---|---|
| Now | [item] | On Track | [owner] | [date] | [dependency] |

### Risks and Dependencies
- [risk or blocker]

### Changes This Update
- [added / moved / cut / reprioritized item]

### Recommended Next Actions
1. [action]
2. [action]
```

