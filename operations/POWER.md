---
name: "operations"
displayName: "Operations"
description: "Operations workflows for vendor reviews, process docs, change requests, capacity planning, status reporting, runbooks, and risk management."
keywords: ["operations", "vendor", "process", "change-management", "capacity-planning", "runbooks", "risk-management", "status-reporting"]
author: "NUX DESIGN"
---

# Operations

Guided operations power for documenting, improving, and running business processes. It supports vendor reviews, process design, change management, capacity planning, status reporting, operational runbooks, and risk-oriented decision support.

This power works standalone when the user provides process context, documents, or team data directly, and it becomes stronger when connected to project trackers, knowledge bases, chat tools, and ITSM systems.

## Steering Index

- `steering/vendor-review.md`: Evaluate vendors for cost, risk, fit, and negotiation leverage.
- `steering/process-documentation.md`: Turn business processes into SOPs with flow, RACI, exceptions, and metrics.
- `steering/change-requests.md`: Create structured change requests with impact analysis, communications, and rollback planning.
- `steering/capacity-planning.md`: Assess utilization, upcoming demand, bottlenecks, and staffing scenarios.
- `steering/status-reporting.md`: Generate concise leadership-ready status reports with KPIs, risks, and decisions needed.
- `steering/runbooks.md`: Create or refine repeatable operational runbooks with prerequisites, exact steps, verification, troubleshooting, and escalation.
- `steering/risk-assessment.md`: Build operational risk registers with likelihood, impact, and mitigation plans.
- `steering/process-optimization.md`: Analyze current-state workflows and design higher-efficiency future-state processes.

## When To Use Which Workflow

- Use `vendor-review.md` when evaluating a new vendor, renewal, replacement, or side-by-side comparison.
- Use `process-documentation.md` when formalizing a process that currently lives in people’s heads or scattered docs.
- Use `change-requests.md` when documenting a change that needs impact analysis, approvals, and rollback planning.
- Use `capacity-planning.md` when forecasting workload, utilization, hiring needs, or delivery constraints.
- Use `status-reporting.md` when summarizing team or project health for leadership or stakeholders.
- Use `runbooks.md` when operational work needs exact repeatable instructions, verification, and escalation paths.
- Use `risk-assessment.md` when evaluating operational risk around a project, vendor, process, or decision.
- Use `process-optimization.md` when a workflow is slow, bottlenecked, high-friction, or heavy on manual work and approvals.

## Standalone Versus Supercharged

This power works well without MCP:

- document processes from direct walkthroughs
- create runbooks and change requests from user input
- assess capacity from team data, spreadsheets, or descriptions
- produce vendor reviews from proposals and contract details

With MCP connected, it becomes stronger through:

- `~~knowledge base`: existing SOPs, policies, runbooks, contracts, and prior reviews
- `~~project tracker`: current workload, milestones, dependencies, and status signals
- `~~chat`: decisions, blockers, coordination context, and stakeholder communications
- `~~ITSM`: incidents, change workflows, ticket relationships, and escalation structures

See `mcp.json` for optional integrations. Every included server is disabled by default so activation is explicit.

## Best Practices

- Start with the current reality, not the idealized version of the process.
- Make risks explicit and tied to owners, mitigations, and timing.
- Prefer specific operational instructions over abstract summaries in runbooks and SOPs.
- Use capacity targets that leave room for interruptions, support load, and context switching.
- When reporting status, surface risk and decisions early rather than hiding them behind green narratives.
