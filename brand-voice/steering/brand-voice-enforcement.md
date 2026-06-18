# Brand Voice Enforcement

Apply existing brand guidelines to content creation and rewriting while keeping voice consistent and adapting tone to the context.

## Primary Use

Use when the user wants to:

- draft content in brand voice
- rewrite content to sound on-brand
- enforce tone and terminology standards
- create sales or marketing content aligned with existing guidelines

## Guideline Loading Order

Look for guidelines in this order:

1. guidelines generated earlier in the current session
2. `.claude/brand-voice-guidelines.md` in the user’s working folder
3. user-provided guidelines pasted or attached directly

If no guidelines are available, stop and tell the user how to generate or provide them.

Also read `.claude/brand-voice.local.md` when available for settings such as strictness and whether explanations should always be included.

## Workflow

### 1. Analyze The Request

Identify:

- content type
- target audience
- format requirements
- key messages
- any requested tone overrides

### 2. Apply Voice Constants

Use the guideline’s stable brand elements:

- "We Are / We Are Not"
- messaging pillars
- preferred terminology
- core personality traits

### 3. Flex Tone By Context

Adjust:

- formality
- energy
- technical depth

based on the intended audience and content format.

### 4. Generate Or Rewrite Content

Produce content that:

- stays within brand boundaries
- uses approved terminology
- aligns with message hierarchy
- reflects guideline examples when useful

### 5. Validate And Explain

After generating content:

- note which brand choices were applied
- explain important tone decisions when helpful
- point out any unresolved guideline ambiguity affecting the draft

## Conflict Handling

When the user’s request conflicts with brand guidance:

1. explain the conflict
2. recommend a path
3. offer options to follow guidelines strictly, adapt them, or override them deliberately

## Open Question Awareness

If the guidelines include unresolved open questions and the current content touches one of them:

- mention that dependency
- apply the stored recommendation by default
- invite the user to override if needed
