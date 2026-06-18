---
name: "engineering"
displayName: "Engineering"
description: "Engineering workflows for standups, code review, debugging, architecture, incident response, deployment readiness, testing, documentation, system design, and technical debt management."
keywords: ["engineering", "code-review", "debugging", "architecture", "incident-response", "deployment", "testing", "documentation", "system-design", "technical-debt"]
author: "NUX DESIGN"
---

# Engineering

Guided engineering power for daily delivery work and operational decision-making. It works as a standalone knowledge power when you provide code, diffs, logs, or system context directly, and it becomes stronger when you connect relevant MCP tools for source control, project tracking, monitoring, incident management, chat, and knowledge bases.

## Steering Index

- `steering/standup.md`: Build concise standup updates from recent work, plans, and blockers.
- `steering/code-review.md`: Review diffs, PRs, or files for security, performance, correctness, and maintainability.
- `steering/debugging.md`: Run a structured reproduce-isolate-diagnose-fix workflow.
- `steering/architecture-decision-records.md`: Create ADRs and evaluate design options with explicit trade-offs.
- `steering/incident-response.md`: Triage incidents, draft updates, and write blameless postmortems.
- `steering/deployment-checklists.md`: Generate pre-deploy, deploy, and rollback checklists.
- `steering/testing-strategy.md`: Design test plans across unit, integration, and end-to-end layers.
- `steering/technical-documentation.md`: Write READMEs, runbooks, API docs, architecture docs, and onboarding guides.
- `steering/system-design.md`: Design systems, APIs, data models, and reliability approaches.
- `steering/technical-debt.md`: Identify, score, and prioritize technical debt with remediation plans.

## When To Use Which Workflow

- Use `standup.md` when you need a daily update formatted as yesterday, today, and blockers.
- Use `code-review.md` before merge, when auditing a risky change, or when reviewing a pasted diff.
- Use `debugging.md` when behavior diverges from expectations and the root cause is unclear.
- Use `architecture-decision-records.md` when comparing options or formalizing a design choice.
- Use `incident-response.md` for live incidents, status updates, severity assessment, or postmortems.
- Use `deployment-checklists.md` before shipping changes, especially when migrations, flags, or rollback risks are involved.
- Use `testing-strategy.md` when deciding what to test, how deeply to test it, and where coverage gaps exist.
- Use `technical-documentation.md` when producing or improving docs for engineers, operators, or new teammates.
- Use `system-design.md` when designing a new service or evaluating boundaries, storage, APIs, or scaling choices.
- Use `technical-debt.md` when building a refactoring backlog or justifying maintenance work.

## Standalone Versus Supercharged

This power works without any MCP tools:

- Paste code, diffs, logs, stack traces, or architecture notes directly.
- Describe your deploy, incident, or testing problem in plain language.
- Ask for structured output such as ADRs, runbooks, checklists, or postmortems.

With MCP tools connected, it can pull richer context automatically:

- Source control: PR diffs, commit history, and branch status.
- Project trackers: ticket status, sprint context, and linked implementation work.
- Monitoring: logs, metrics, alerts, and deploy correlations.
- Incident tools: paging context and incident record updates.
- Chat and knowledge systems: relevant discussions, prior ADRs, runbooks, and standards.

See `mcp.json` for optional integrations. All are disabled by default so you can opt in explicitly.

## Best Practices

- Give exact inputs when possible: raw error text, PR links, stack traces, release names, or concrete requirements.
- State constraints early: timelines, scale, compliance, user impact, and rollback sensitivity change the right answer.
- Prefer structured outputs: standups, ADRs, postmortems, and checklists are most useful when kept concise and decision-oriented.
- Use connected tools to gather context, not to replace engineering judgment.
- Keep documentation, test plans, and debt backlogs current enough to support operational work.
