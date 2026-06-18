---
name: "human-resources"
displayName: "Human Resources"
description: "People-operations workflows for recruiting, offers, onboarding, performance reviews, policy guidance, compensation analysis, org planning, and people reporting."
keywords: ["hr", "people-ops", "recruiting", "offers", "onboarding", "performance", "compensation", "policy", "org-design"]
author: "NUX DESIGN"
---

# Human Resources Power

A human-resources power for Kiro focused on practical people-operations workflows: recruiting pipeline visibility, interview preparation, offer drafting, onboarding plans, performance reviews, policy guidance, compensation analysis, org planning, and people analytics reporting.

This power works as a knowledge-first power with manual inputs, uploaded data, and pasted policy content. It becomes stronger when you connect knowledge bases, chat, calendars, and other systems that provide live people-operations context.

## Available Steering Files

| File | Use When |
|------|----------|
| `draft-offer.md` | Drafting an offer letter, framing total compensation, or preparing negotiation notes for a hiring manager |
| `onboarding.md` | Creating a pre-start checklist, Day 1 schedule, Week 1 plan, or 30/60/90 goals for a new hire |
| `performance-review.md` | Building self-assessment templates, manager reviews, or calibration prep docs |
| `policy-lookup.md` | Answering handbook or benefits questions in plain language with cited sources |
| `comp-analysis.md` | Benchmarking pay, analyzing band placement, or modeling equity and total compensation |
| `people-report.md` | Producing headcount, attrition, diversity, or org-health reports from people data |
| `recruiting-pipeline.md` | Tracking candidate flow, stage conversions, time to fill, and source effectiveness |
| `interview-prep.md` | Designing structured interviews, question banks, rubrics, and debrief templates |
| `org-planning.md` | Planning headcount, org structure, sequencing, and span-of-control tradeoffs |

## When to Use Each Workflow

- Use `draft-offer.md` when a candidate is ready for an offer or comp package review.
- Use `onboarding.md` when a new hire start date exists and the team needs a complete onboarding plan.
- Use `performance-review.md` during review season or when translating vague feedback into a structured review artifact.
- Use `policy-lookup.md` when someone asks about PTO, leave, expenses, remote work, benefits, or other handbook topics.
- Use `comp-analysis.md` when pricing a new role, reviewing internal band placement, or modeling equity changes.
- Use `people-report.md` when leadership needs org snapshots, attrition analysis, or diversity metrics.
- Use `recruiting-pipeline.md` when the hiring team needs candidate-stage visibility and funnel metrics.
- Use `interview-prep.md` when a role needs a consistent interview plan and scorecard.
- Use `org-planning.md` when rethinking headcount, reporting lines, or team design.

## Standalone vs Supercharged

Every workflow works without connectors:

| Workflow | Standalone | Supercharged With |
|----------|-----------|-------------------|
| Offers | Manual role, level, comp, and benefits details | HRIS, ATS, knowledge base |
| Onboarding | New-hire details and role context | Knowledge base, calendar, HRIS |
| Performance reviews | Manual goals, feedback, and employee context | HRIS, project tracker, docs |
| Policy lookup | Pasted handbook excerpts | Knowledge base, HRIS |
| Compensation analysis | Uploaded CSVs or described bands | Compensation datasets, HRIS |
| People reports | Uploaded workforce data | HRIS, chat for distribution |
| Recruiting pipeline | Manual candidate and stage lists | ATS |
| Interview prep | Role and competency context | ATS, knowledge base |
| Org planning | Current org notes and headcount goals | HRIS, planning docs |

## Optional MCP Integrations

The repo’s live MCP config only includes a few usable connectors, but they add real value:

| Category | Examples | What It Enables |
|----------|----------|-----------------|
| Chat | Slack | Team announcements, coordination, report sharing |
| Knowledge base | Notion, Atlassian | Handbook search, onboarding docs, templates, decision records |

Connector categories mentioned in the source docs but not concretely configured include HRIS, ATS, calendar, email, and compensation-data systems. Treat those as optional conceptual integrations rather than included live MCP definitions.

See [mcp.json](/Users/Niwat.yah/Kiro Powers/human-resources/mcp.json). All included servers are disabled by default.

## Best Practices

1. Cite policy sources explicitly. For HR questions, ambiguity is risk.
2. Keep compensation analysis clear about data freshness, source quality, and confidence.
3. Use structured rubrics for hiring and reviews; avoid gut-feel evaluation.
4. Treat uploaded people data as sensitive and avoid unnecessary reproduction of raw details.
5. Separate operational guidance from legal advice. Escalate edge cases to HR, legal, or finance where appropriate.
