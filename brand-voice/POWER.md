---
name: "brand-voice"
displayName: "Brand Voice"
description: "Discover brand signals, generate reusable voice guidelines, and enforce brand-consistent writing across content workflows. Best for teams whose brand knowledge is scattered across documents, design files, and conversation systems."
keywords: ["brand-voice", "brand-guidelines", "messaging", "tone-of-voice", "copy-review", "content-rewriting", "notion", "figma"]
author: "NUX DESIGN"
---

# Brand Voice

Guided MCP power for discovering scattered brand materials, synthesizing them into actionable brand guidelines, and enforcing those guidelines across AI-generated content. It is designed for teams whose brand knowledge is fragmented across documents, wikis, transcripts, design systems, and conversation tools.

This power is strongest when connected to enterprise content and conversation platforms, because its core value comes from discovery, triage, and synthesis across those sources.

## Onboarding

Start with one of these situations:

- you need to find brand guidance that is scattered across tools
- you already have source materials and want a durable guidelines document
- you have existing brand guidelines and want new content rewritten to match them

Best results come from providing:

- target audience and channel
- example content that feels on-brand and off-brand
- any existing style guide, messaging doc, or pitch deck
- access to connected systems such as Notion, Confluence, Box, or Figma when discovery matters

## Available Steering Files

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

## Available MCP Servers

This power includes the following MCP server definitions in [mcp.json](/Users/Niwat.yah/Kiro Powers/brand-voice/mcp.json):

| Server | Status | Purpose |
|--------|--------|---------|
| `notion` | Disabled by default | Search existing brand docs, strategy pages, and internal guidance |
| `atlassian` | Disabled by default | Pull Confluence pages and related project context |
| `box` | Disabled by default | Access stored decks, documents, and marketing assets |
| `figma` | Disabled by default | Inspect design-system content and branded visual language |
| `gong` | Disabled by default | Analyze call transcripts for recurring messaging and tone |
| `granola` | Disabled by default | Pull meeting notes and synthesis inputs for voice discovery |

## Configuration

All bundled MCP servers are disabled by default.

Enable only the systems that actually contain brand evidence for your team. In most cases:

1. enable document sources first, such as Notion, Confluence, or Box
2. add Figma when visual language or design-system wording matters
3. add conversation sources such as Gong or Granola when spoken tone or messaging patterns matter

If no MCP servers are enabled, this power still works from pasted guidelines, transcript excerpts, screenshots, and manually supplied brand examples.

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

## Troubleshooting

### Discovery results are weak or noisy

- connect higher-signal sources first, such as formal docs and pitch decks
- provide examples of content that is definitely on-brand
- narrow the search by audience, product line, or channel

### Rewrites feel generic

- provide stronger source examples or an explicit guidelines document
- specify the audience, format, and level of formality
- separate permanent voice traits from channel-specific tone choices

### Connected systems do not contain enough brand evidence

- fall back to pasted documents, messaging frameworks, transcripts, and approved copy
- treat the result as a draft guideline set and mark low-confidence areas clearly
