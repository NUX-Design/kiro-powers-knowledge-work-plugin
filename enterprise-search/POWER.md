---
name: enterprise-search
description: Cross-tool search and digest workflows for chat, email, documents, wikis, trackers, and other connected enterprise sources.
version: 1.3.0
author: Anthropic
---

# Enterprise Search

Guided MCP power for searching across company tools as if they were one knowledge base. It is built around connected MCP sources and is most valuable when multiple systems are available, such as chat, email, cloud storage, knowledge bases, and project trackers.

This power is designed to decompose a question, query multiple connected systems in parallel, deduplicate overlapping results, and synthesize a single answer with source attribution.

## Steering Index

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

See `mcp.json` for optional integrations. Every included server is disabled by default so activation remains explicit.

## Best Practices

- Connect multiple sources before relying on answers for decisions or status.
- Use clear time bounds, people names, and project names when possible to improve ranking quality.
- Prefer synthesized answers with attribution over raw result dumps.
- Surface uncertainty when sources conflict or are outdated.
- Treat missing or rate-limited systems as scope gaps and call them out explicitly.
