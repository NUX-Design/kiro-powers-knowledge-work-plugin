---
name: "enterprise-search"
displayName: "Enterprise Search"
description: "Search across connected company systems, synthesize findings, and generate cross-source digests with attribution. Best for questions that span chat, docs, trackers, and other enterprise knowledge sources."
keywords: ["enterprise-search", "cross-source-search", "knowledge-synthesis", "team-digest", "slack", "notion", "atlassian", "asana"]
author: "Anthropic"
---

# Enterprise Search

Guided MCP power for searching across company tools as if they were one knowledge base. It is built around connected MCP sources and is most valuable when multiple systems are available, such as chat, email, cloud storage, knowledge bases, and project trackers.

This power is designed to decompose a question, query multiple connected systems in parallel, deduplicate overlapping results, and synthesize a single answer with source attribution.

## Onboarding

Start with one of these requests:

- find an answer that may live across several tools
- catch up on activity across projects or teams
- build a search plan before querying multiple systems
- reconcile overlapping or conflicting results from different sources

Best results come from providing:

- time range
- project, team, or topic name
- people names
- source preferences if some systems are more trusted than others

## Available Steering Files

- `steering/search.md`: Search across connected sources with unified filters and synthesized answers.
- `steering/digests.md`: Generate daily or weekly cross-source digests grouped by topic.
- `steering/search-strategy.md`: Decompose natural-language questions into source-specific search plans.
- `steering/source-management.md`: Detect available sources, guide connection gaps, and handle source priority and rate limits.
- `steering/knowledge-synthesis.md`: Merge, rank, deduplicate, and attribute results from multiple systems.

## When To Use Which Workflow

- Use `search.md` when looking for a decision, conversation, document, expert, status update, or historical reference across tools.
- Use `digests.md` when catching up after time away or summarizing activity across projects and systems.
- Use `search-strategy.md` when you need the query-planning logic for ambiguous, cross-source, or filtered searches.
- Use `source-management.md` when the answer quality depends on which sources are connected or when some systems are unavailable.
- Use `knowledge-synthesis.md` when multiple sources return overlapping, conflicting, or incomplete information that must be reconciled into one answer.

## Standalone Versus Supercharged

This power is fundamentally MCP-driven. Without connected sources, it can explain the workflow and identify what kinds of tools should be connected, but it cannot deliver real enterprise search results.

With MCP connected, it can search and synthesize across:

- `~~chat`: channels, threads, DMs, and discussion history
- `~~email`: mail threads, senders, attachments, and conversations
- `~~cloud storage`: docs, sheets, slides, PDFs, and file metadata
- `~~knowledge base`: wiki pages, knowledge articles, runbooks, and policies
- `~~project tracker`: tasks, issues, epics, milestones, and comments
- other MCP-connected systems such as CRM or ticketing platforms

## Available MCP Servers

This power includes the following MCP server definitions in [mcp.json](/Users/Niwat.yah/Kiro Powers/enterprise-search/mcp.json):

| Server | Status | Purpose |
|--------|--------|---------|
| `slack` | Disabled by default | Search channels, threads, DMs, and discussion history |
| `notion` | Disabled by default | Search team docs, notes, policies, and internal knowledge |
| `guru` | Disabled by default | Search internal knowledge cards and curated answers |
| `atlassian` | Disabled by default | Search Jira and Confluence for tickets, pages, and project context |
| `asana` | Disabled by default | Search work items, comments, and project status context |

## Configuration

All bundled MCP servers are disabled by default.

For the best results:

1. enable at least two complementary sources, such as Slack plus Notion or Atlassian
2. prefer sources that cover both conversation history and durable documentation
3. expand the source set only when it improves answer quality rather than adding noise

If no MCP servers are enabled, this power can still help plan search strategy, define source gaps, and describe what should be connected, but it cannot perform real enterprise search.

## Best Practices

- Connect multiple sources before relying on answers for decisions or status.
- Use clear time bounds, people names, and project names when possible to improve ranking quality.
- Prefer synthesized answers with attribution over raw result dumps.
- Surface uncertainty when sources conflict or are outdated.
- Treat missing or rate-limited systems as scope gaps and call them out explicitly.

## Troubleshooting

### Search results are incomplete

- check whether the highest-value systems are actually connected
- narrow the question with dates, teams, project names, or people
- note missing systems explicitly so the answer is framed with the right scope

### Results are noisy or repetitive

- use `search-strategy.md` to tighten source selection and query shape
- prefer fewer high-signal systems before querying everything
- synthesize overlapping results instead of listing duplicates

### Sources disagree

- treat the answer as a synthesis problem, not a search-only problem
- compare timestamps, ownership, and source authority
- explain uncertainty and point out which source is most trustworthy for the question
