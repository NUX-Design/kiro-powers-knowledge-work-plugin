# Memory Management

Build a two-tier workplace memory system so requests in internal shorthand can be decoded accurately.

## Goal

Translate shorthand like names, acronyms, internal terms, and project codenames into useful context without repeated clarification.

## Architecture

- `CLAUDE.md`: hot cache for frequently used people, terms, projects, and preferences
- `memory/glossary.md`: full decoder ring
- `memory/people/`: detailed people profiles
- `memory/projects/`: detailed project notes
- `memory/context/`: company, teams, tools, and process context

## Lookup Flow

1. check `CLAUDE.md`
2. check `memory/glossary.md`
3. check richer project or people files
4. ask the user when meaning is still unknown

## What To Store

### In `CLAUDE.md`

- the user’s role and context
- top people
- common acronyms and terms
- active projects
- working preferences

### In `memory/`

- full glossary
- aliases and nicknames
- detailed people context
- project status and stakeholders
- company tools and processes

## Update Rules

- add glossary terms when shorthand recurs
- create or extend people and project files as new context appears
- keep `CLAUDE.md` compact enough to serve as a hot cache
- use deeper files for long-tail detail

## Best Practices

- capture how people are actually referred to, not just formal names
- cross-link relationships between people, tasks, and projects
- treat memory as a living system that evolves with work context
