# Source Management

Manage connected enterprise sources for search quality, availability, and user guidance.

## Detecting Connected Sources

Infer which source categories are available by checking for corresponding MCP tool capabilities.

Typical source categories:

- `~~chat`
- `~~email`
- `~~cloud storage`
- `~~project tracker`
- `~~CRM`
- `~~knowledge base`

## Guiding Connection Gaps

When few or no sources are connected:

- name what is currently available
- explain what additional source categories would improve coverage
- tell the user to connect missing systems in MCP settings

When a specific tool is requested but not connected, state that clearly and explain that it must be added before future searches can include it.

## Source Priority

Use source priority for weighting, not for excluding relevant sources.

Examples:

- decision queries prioritize conversations and follow-up confirmations
- status queries prioritize trackers and recent updates
- document queries prioritize cloud storage and knowledge bases
- policy queries prioritize official documentation

## Rate Limits And Failures

If a source is rate limited or unreachable:

1. do not block the entire workflow
2. continue with remaining sources
3. tell the user what was excluded
4. suggest retrying later when appropriate

## Source Health Reporting

When useful, summarize the search scope by naming:

- available sources
- unavailable sources
- rate-limited sources

This helps users understand how complete the answer really is.
