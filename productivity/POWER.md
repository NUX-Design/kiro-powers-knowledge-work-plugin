---
name: "productivity"
displayName: "Productivity"
description: "Personal productivity workflows for tasks, workplace memory, daily updates, and connected work context."
keywords: ["productivity", "tasks", "memory", "daily-updates", "organization", "workflow"]
author: "Anthropic"
---

# Productivity

Guided productivity power for managing tasks, maintaining workplace memory, and staying current across active workstreams. It combines local file-based organization with optional MCP-powered sync from chat, knowledge, and project tools.

This power is especially useful when you want a persistent system built around `TASKS.md`, `CLAUDE.md`, and a `memory/` directory, while still benefiting from connected external systems when available.

## Steering Index

- `steering/start.md`: Initialize tasks, memory, and orientation for the productivity system.
- `steering/update.md`: Refresh tasks, triage stale items, and fill memory gaps from current activity.
- `steering/task-management.md`: Maintain a shared markdown task list in `TASKS.md`.
- `steering/memory-management.md`: Build a two-tier workplace memory system using `CLAUDE.md` and `memory/`.

## When To Use Which Workflow

- Use `start.md` when setting up the productivity workflow for the first time or re-initializing missing files.
- Use `update.md` for regular syncs, stale-task review, and optional deeper activity scans.
- Use `task-management.md` whenever reading, adding, updating, triaging, or completing tasks in `TASKS.md`.
- Use `memory-management.md` when decoding workplace shorthand, storing key context, and teaching the system who people and projects are.

## Standalone Versus Supercharged

This power works well without MCP:

- maintain `TASKS.md` locally
- build `CLAUDE.md` and `memory/` from direct conversation
- organize people, acronyms, projects, and commitments manually

With MCP connected, it becomes more useful for:

- `~~chat`: surfacing mentions, commitments, and team context
- `~~knowledge base`: pulling reference documents and definitions
- `~~project tracker`: syncing assigned work and spotting stale tasks
- other connected work systems that expose actionable context

See `mcp.json` for optional integrations. Every included server is disabled by default so you can opt in explicitly.

## Dashboard Note

The source plugin includes a local `dashboard.html` asset for a visual task and memory view. This power documents the workflow conceptually in steering files but does not copy the dashboard asset into the power package.

## Best Practices

- Keep `TASKS.md` in the current working directory and use it as the canonical shared task list.
- Capture workplace shorthand as soon as it appears often enough to matter.
- Prefer a lean `CLAUDE.md` hot cache and push full detail into `memory/`.
- Review stale tasks regularly instead of letting the active list accumulate dead items.
- Treat connected sources as discovery aids, not as permission to auto-commit task or memory changes without review.
