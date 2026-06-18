---
name: "product-management"
displayName: "Product Management"
description: "Product workflows for specs, roadmaps, sprint planning, stakeholder communication, research synthesis, competitive analysis, metrics review, and product brainstorming."
keywords: ["product", "pm", "roadmap", "prd", "research", "metrics", "competitive-analysis", "stakeholder-updates", "sprint-planning"]
author: "Anthropic"
---

# Product Management Power

A product management power for Kiro that covers the core PM workflow: writing specs, planning roadmaps and sprints, communicating with stakeholders, synthesizing user research, analyzing competitors, reviewing metrics, and pressure-testing ideas through structured brainstorming.

This power works as a standalone knowledge power when you provide context directly. It gets stronger when you connect project trackers, knowledge bases, design systems, analytics, feedback tools, chat, and meeting-transcription sources.

## Available Steering Files

| File | Use When |
|------|----------|
| `write-spec.md` | Turning a feature idea or problem statement into a scoped PRD or feature spec |
| `roadmap-update.md` | Creating, updating, or reprioritizing a roadmap |
| `sprint-planning.md` | Planning a sprint around capacity, priorities, and dependencies |
| `stakeholder-update.md` | Writing status updates for executives, engineering, partners, customers, or launch audiences |
| `synthesize-research.md` | Converting interviews, surveys, feedback, and analytics into findings and recommendations |
| `competitive-brief.md` | Building a competitor or feature-area analysis brief |
| `metrics-review.md` | Reviewing product health metrics, trends, targets, and actions |
| `product-brainstorming.md` | Exploring problems, generating ideas, and challenging assumptions as a thinking partner |

## When to Use Each Workflow

- Use `write-spec.md` when the input is still fuzzy and needs to become a crisp, scoped product document.
- Use `roadmap-update.md` when priorities shift, timelines move, or a roadmap needs to be built from scratch.
- Use `sprint-planning.md` when a team needs a realistic sprint goal, backlog shape, and capacity view.
- Use `stakeholder-update.md` when the same underlying progress needs to be translated for different audiences.
- Use `synthesize-research.md` when raw user input needs to become themes, personas, opportunities, and product implications.
- Use `competitive-brief.md` when product strategy, positioning, feature parity, or sales enablement needs market context.
- Use `metrics-review.md` when numbers need interpretation, not just reporting.
- Use `product-brainstorming.md` when a PM needs a sharp sparring partner before converging on a direction.

## Standalone vs Supercharged

Every workflow can run without connectors:

| Workflow | Standalone | Supercharged With |
|----------|-----------|-------------------|
| Specs | Problem statement, notes, screenshots, constraints | Project tracker, knowledge base, design tools |
| Roadmaps | Pasted roadmap, spreadsheet, or prose | Project trackers, docs, chat |
| Sprint planning | Team availability and backlog pasted in | Tracker, calendar, chat |
| Stakeholder updates | Manual progress summary | Tracker, chat, meeting notes, docs |
| Research synthesis | Notes, transcripts, survey exports | Feedback tools, analytics, knowledge base, meeting transcription |
| Competitive analysis | User-provided competitor context | Web research, knowledge base, chat, competitive-intelligence sources |
| Metrics review | Metric tables, screenshots, or targets | Product analytics tools |
| Brainstorming | Problem statement or strategic question | Prior research, docs, roadmap context |

## Optional MCP Integrations

These connectors materially improve this power and are included as opt-in definitions:

| Category | Examples | What It Enables |
|----------|----------|-----------------|
| Project tracker | Linear, Asana, monday.com, ClickUp, Atlassian | Pull roadmap items, backlog status, milestones, dependencies |
| Knowledge base | Notion | Existing specs, research, decisions, meeting notes |
| Design | Figma | Design context, mocks, component references |
| Product analytics | Amplitude, Pendo | Metrics pulls, trends, segment breakdowns |
| User feedback | Intercom | Tickets, requests, conversation themes |
| Chat | Slack | Stakeholder context, blocker threads, competitive mentions |
| Meeting transcription | Fireflies | Meeting notes, decisions, interview summaries |
| Competitive intelligence | Similarweb | Market and traffic context for competitor research |

See [mcp.json](/Users/Niwat.yah/Kiro Powers/product-management/mcp.json). All included servers are disabled by default.

## Best Practices

1. Start with the decision the work should inform. A PM artifact without a decision target usually bloats.
2. Be explicit about constraints: user segment, deadlines, dependencies, metrics, and resourcing change the right answer.
3. Keep outputs opinionated. This power should help prioritize and cut scope, not just restate inputs.
4. Prefer structured evidence over intuition when possible. Research, metrics, and prior decisions should shape recommendations.
5. Separate discovery from commitment. Brainstorm widely first, then converge with explicit tradeoffs.
