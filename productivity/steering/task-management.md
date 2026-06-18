# Task Management

Use a shared `TASKS.md` file in the current working directory as the canonical task list.

## File Rules

- always use `TASKS.md` in the current working directory
- if it does not exist, create it with the standard template

## Template

```markdown
# Tasks

## Active

## Waiting On

## Someday

## Done
```

## Task Format

- active or waiting task: `- [ ] **Task title** - context, for whom, due date`
- completed task: `- [x] ~~Task~~ (date)`
- sub-bullets for additional details

## Common Interactions

- summarize what is active or waiting
- add tasks from direct requests
- mark tasks done and move them to `Done`
- review overdue or waiting items
- offer to capture action items from meetings or conversations

## Conventions

- bold task titles
- include who the task is for when relevant
- include due dates when known
- include waiting-since markers when relevant
- keep the done section short-lived and periodically clear older completions
