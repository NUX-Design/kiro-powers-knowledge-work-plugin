# Search Strategy

Break a natural-language question into source-specific searches and orchestrate them in parallel.

## Query Classification

Identify the query type first:

- decision
- status
- document
- person
- factual or policy
- temporal
- exploratory

Query type determines weighting and source priority.

## Extract Search Components

Pull out:

- required keywords
- entities
- time markers
- source hints
- filters
- negations

## Source-Specific Translation

For each connected source, generate one or more search variants.

Prefer semantic search for:

- conceptual questions
- exploratory prompts
- vague language

Prefer keyword search for:

- exact phrases
- acronyms
- filter-heavy queries
- known project names

Generate alternate phrasings when users may refer to the same concept differently.

## Ranking Guidance

Weight results differently depending on the question:

- decision queries: freshness and conversational evidence matter
- status queries: trackers and recency matter most
- document queries: document stores and knowledge bases matter most
- factual queries: authority matters most

## Ambiguity Handling

Ask one focused clarifying question only when there are clearly distinct interpretations that would lead to materially different search plans.

## Fallback Strategy

If the initial query is too narrow:

1. broaden date ranges
2. remove location filters
3. reduce non-essential keywords
4. keep the core entity or topic terms

Always search sources in parallel rather than sequentially.
