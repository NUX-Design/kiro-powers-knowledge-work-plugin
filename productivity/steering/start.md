# Productivity Start

Initialize the task and memory system, then orient the user to how the workflow operates.

## Initialization Checklist

Check for:

- `TASKS.md`
- `CLAUDE.md`
- `memory/`

If `TASKS.md` is missing, create it using the standard task template.

If `CLAUDE.md` and `memory/` are missing, treat this as a fresh memory bootstrap.

## User Orientation

If the system is already initialized, explain that tasks and memory are loaded and point the user to the update workflow.

If memory is not yet bootstrapped:

1. ask where the user keeps tasks or todos
2. inspect real tasks to learn workplace shorthand
3. decode nicknames, acronyms, projects, and jargon interactively
4. offer an optional broader scan of available work systems

## Memory Bootstrap Outputs

Create:

- `CLAUDE.md` as working memory
- `memory/glossary.md`
- `memory/people/`
- `memory/projects/`
- `memory/context/company.md`

## Reporting

Summarize what was created and how many tasks, people, terms, and projects were captured.
