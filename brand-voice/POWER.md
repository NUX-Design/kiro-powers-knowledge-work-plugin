---
name: brand-voice
description: Brand discovery, guideline generation, and brand-aligned content enforcement across enterprise knowledge sources.
version: 1.1.0
author: Tribe AI
---

# Brand Voice

Guided MCP power for discovering scattered brand materials, synthesizing them into actionable brand guidelines, and enforcing those guidelines across AI-generated content. It is designed for teams whose brand knowledge is fragmented across documents, wikis, transcripts, design systems, and conversation tools.

This power is strongest when connected to enterprise content and conversation platforms, because its core value comes from discovery, triage, and synthesis across those sources.

## Steering Index

- `steering/discover-brand.md`: Search connected platforms for brand materials and produce a structured discovery report.
- `steering/guideline-generation.md`: Convert discovery findings, documents, and transcripts into LLM-ready brand guidelines with confidence scoring.
- `steering/brand-voice-enforcement.md`: Apply existing brand guidelines to content generation and rewriting while keeping voice constant and tone context-aware.

## When To Use Which Workflow

- Use `discover-brand.md` when the user wants to find style guides, pitch decks, transcript patterns, messaging artifacts, or any other brand material spread across systems.
- Use `guideline-generation.md` when the user already has a discovery report, source documents, or transcripts and wants a durable brand guideline document.
- Use `brand-voice-enforcement.md` when drafting or rewriting emails, proposals, landing pages, social posts, presentations, or other customer-facing content to match the brand.

## Standalone Versus Supercharged

This power can work in a limited standalone mode if the user directly provides brand documents, transcript excerpts, or explicit style guidance.

With MCP connected, it becomes materially stronger because it can discover and cross-check brand patterns across:

- Notion
- Atlassian / Confluence
- Box
- Figma
- Gong
- Granola

The source plugin also notes native integrations such as Google Drive and Slack conceptually, but this power only includes the MCP-connected systems actually defined in the source `mcp.json`.

## File And Settings Conventions

The source plugin relies on project-local files such as:

- `.claude/brand-voice.local.md` for configuration
- `.claude/brand-voice-guidelines.md` for saved guidelines

This power preserves those conventions conceptually in the steering workflows.

## Best Practices

- Run discovery before guideline generation unless the user already has strong source material assembled.
- Prefer document-storage systems as the primary discovery backbone, then use transcripts and chat-style sources as supporting evidence.
- Surface ambiguity as open questions with recommendations instead of forcing false certainty.
- Keep voice constant and let tone flex by audience, channel, and context.
- Save guidelines in a predictable location so downstream enforcement can reuse them consistently.
