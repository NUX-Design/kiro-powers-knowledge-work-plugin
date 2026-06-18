# Write Spec

Use this workflow to turn a vague idea, feature request, or product problem into a structured PRD or feature spec.

## Inputs

Accept any of:

- Feature name
- Problem statement
- User request
- High-level idea

## Workflow

### 1. Understand the Feature

Start with the most important missing context:

- What problem is being solved?
- Who has the problem?
- Why now?

Do not dump every question at once. Fill gaps conversationally.

### 2. Gather Context

Collect:

- User problem
- Target users or segments
- Success metrics
- Constraints such as timeline, technical limits, regulatory needs, or dependencies
- Prior attempts or existing solutions

### 3. Pull Connected Context When Available

If tools are connected, look for:

- Related tickets or epics in a project tracker
- Prior specs, research, or decision docs in a knowledge base
- Design explorations or mocks in design tools

If tools are not connected, proceed from user-provided context only.

### 4. Generate the Spec

Include:

- Problem statement
- Goals
- Non-goals
- User stories
- Requirements
- Success metrics
- Open questions
- Timeline considerations

## Section Guidance

### Problem Statement

- 2 to 3 sentences
- Who is affected
- Why it matters
- Cost of not solving it

### Goals

- 3 to 5 measurable outcomes
- Separate user outcomes from business outcomes where useful
- Prefer outcomes over output language

### Non-Goals

- 3 to 5 explicit out-of-scope items
- Briefly explain why each is excluded

### User Stories

Use:

`As a [user type], I want [capability] so that [benefit]`

Rules:

- Keep the user type specific
- Describe capability, not UI implementation
- Include key edge cases
- Group by persona if needed

### Requirements

Categorize as:

- Must-have / P0
- Nice-to-have / P1
- Future considerations / P2

Each requirement should be clear, testable, and tied to acceptance criteria.

### Success Metrics

Include both:

- Leading indicators such as adoption, activation, completion, error rate
- Lagging indicators such as retention, revenue, support load, satisfaction

Targets should be specific and time-bound.

### Open Questions

- Tag who should answer each question
- Distinguish blocking vs non-blocking questions

### Timeline Considerations

- Hard deadlines
- Dependencies
- Suggested phasing if needed

## Acceptance Criteria

Use either:

- Given / When / Then
- Checklist format

Acceptance criteria should cover:

- Happy path
- Error states
- Edge cases
- Negative cases

## Scope Management Rules

- Be ruthless about P0 scope.
- If the request is too large, split it into phases and spec phase one.
- Use explicit non-goals to prevent scope creep.

## Output Format

```markdown
## [Feature Name]

### Problem Statement
[text]

### Goals
- [goal]

### Non-Goals
- [non-goal]

### User Stories
- As a [user], I want [capability] so that [benefit]

### Requirements
#### Must-Have (P0)
- [requirement]

#### Nice-to-Have (P1)
- [requirement]

#### Future Considerations (P2)
- [requirement]

### Acceptance Criteria
- [criterion]

### Success Metrics
- [metric and target]

### Open Questions
- [question] — [owner]

### Timeline Considerations
- [deadline or dependency]
```

