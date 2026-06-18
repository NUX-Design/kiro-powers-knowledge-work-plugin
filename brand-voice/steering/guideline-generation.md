# Guideline Generation

Turn discovery findings, documents, transcripts, and direct input into LLM-ready brand voice guidelines with confidence scoring and open questions.

## Accepted Inputs

- discovery report
- uploaded brand documents
- conversation transcripts
- direct user input about voice and values

If a discovery report exists, use it as the primary input because it already contains ranked and triaged sources.

## Workflow

### 1. Identify Sources

Determine what inputs are available. If none are available:

- check for an earlier discovery report
- check known settings locations
- suggest running discovery first

### 2. Process Source Types

For each source class, extract:

- voice attributes
- messaging themes
- terminology
- tone signals
- examples
- conflicts

### 3. Synthesize The Guideline Document

Generate a durable guideline structure with sections such as:

- brand personality
- voice attributes
- messaging themes
- terminology standards
- "We Are / We Are Not"
- voice constants versus tone flexes
- tone-by-context matrix

### 4. Assign Confidence

Mark sections with:

- high confidence
- medium confidence
- low confidence

Base confidence on source count, corroboration, explicitness, and conflict level.

### 5. Surface Open Questions

For unresolved ambiguity, produce open questions that include:

- what was found
- why it is ambiguous
- the recommended resolution
- what the team needs to confirm or override

### 6. Quality Check

Before finalizing, confirm:

- major sections are populated when evidence supports them
- multiple voice attributes exist
- tone guidance covers multiple contexts
- confidence levels are assigned
- source attribution exists for important conclusions
- no sensitive information is exposed unnecessarily

### 7. Save For Reuse

If the user’s working folder is available, save guidelines to:

- `.claude/brand-voice-guidelines.md`

If a prior file exists, archive it with a dated filename before replacing it.

## Output Expectations

Provide:

- the generated guideline summary
- confidence breakdown
- strongest brand signals
- open questions, if any
- path where the guidelines were saved, when saved successfully
