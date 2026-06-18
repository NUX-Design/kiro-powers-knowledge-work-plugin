# Brand Discovery

Search connected enterprise platforms for brand materials, rank what matters, and produce a discovery report with conflicts and open questions.

## Primary Purpose

Use this workflow when the user wants to:

- discover brand materials
- find style guides
- audit brand content
- locate voice, tone, or messaging documents
- understand what brand artifacts already exist

## Workflow

### 1. Orient The User

Explain that the process will:

1. search connected platforms
2. analyze and rank findings
3. generate a structured discovery report
4. optionally chain into guideline generation later

Wait for confirmation before starting.

### 2. Check Settings

If available, read `.claude/brand-voice.local.md` for:

- company name
- enabled platforms
- search depth
- max sources
- known brand material locations

### 3. Validate Platform Coverage

Separate sources into:

- document platforms
- supplementary platforms such as transcripts, meetings, and design systems

Rules:

- stop if no document platforms are connected
- warn if only supplementary platforms are available
- warn when discovery scope is too narrow for high-confidence synthesis

### 4. Confirm Search Scope

Confirm briefly:

- which platforms to search
- whether to include transcripts and supplementary platforms
- whether to prioritize any known locations

### 5. Run Discovery

Search across connected sources and produce:

- discovered materials
- source categories
- ranked and triaged findings
- conflicts
- gaps
- open questions with recommendations

### 6. Present Report

Summarize:

- total sources found
- strongest brand elements
- conflicts or inconsistencies
- unresolved questions

### 7. Offer Next Steps

- generate guidelines
- resolve open questions first
- save the report
- expand search scope

## Error Handling

- if no platforms are connected, explain what kinds of systems should be added
- if searches return little coverage, flag low-confidence discovery and suggest manual input
- if permissions fail on one platform, continue with the rest and state the gap
