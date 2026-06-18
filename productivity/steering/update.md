# Productivity Update

Refresh tasks and memory from current state and optionally run a broader activity scan.

## Modes

- default update
- comprehensive update

## Default Update Workflow

1. load `TASKS.md` and `memory/`
2. sync tasks from available external sources when present
3. triage stale or overdue items
4. decode task entities and detect memory gaps
5. ask about unknown people, projects, or acronyms
6. enrich memory with links, status changes, and relationships
7. report the changes made or suggested

## Comprehensive Mode

Run everything in default mode, plus scan connected sources such as:

- chat
- email
- calendar
- documents

Then:

- identify likely missing tasks
- suggest new people, projects, and topics for memory
- group findings by confidence

## Important Rules

- do not auto-add tasks without confirmation
- do not auto-add memory entries without confirmation
- preserve source links when available
- keep the workflow interactive when uncertainty is high
