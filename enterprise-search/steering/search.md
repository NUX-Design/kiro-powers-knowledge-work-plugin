# Unified Search

Search across all connected MCP sources in a single query. Decompose the user’s request, run parallel searches, and synthesize the results into one answer with attribution.

## Workflow

### 1. Check Available Sources

Determine which source categories are connected, such as:

- `~~chat`
- `~~email`
- `~~cloud storage`
- `~~project tracker`
- `~~CRM`
- `~~knowledge base`

If none are connected, explain that search requires at least one connected source and name the categories that can be added.

### 2. Parse The Query

Extract:

- intent
- entities
- time constraints
- source hints
- filters such as `from:`, `in:`, `after:`, `before:`, `type:`

### 3. Decompose Into Sub-Queries

Create targeted searches per available source using each tool’s native capabilities.

Examples:

- `~~chat`: sender, channel, thread, time-window, or semantic chat search
- `~~email`: sender, subject, attachment, and date filters
- `~~cloud storage`: file title, file type, full text, and modified date
- `~~project tracker`: task text, assignee, project, or modification date
- `~~knowledge base`: semantic or keyword document search

### 4. Execute In Parallel

Search all relevant sources at the same time. A failure in one source must not block others.

### 5. Rank And Deduplicate

Rank by:

- relevance
- freshness
- authority
- completeness

Merge the same fact or decision when it appears across multiple sources.

### 6. Present Unified Results

Lead with the answer, not the search process. Provide source attribution and note whether the result is direct, exploratory, or partial.

## Edge Cases

- Ask one clarifying question only when ambiguity would materially change the search.
- If no results are found, suggest broader terms or time ranges.
- If some sources fail, return partial results and name the missing coverage.
