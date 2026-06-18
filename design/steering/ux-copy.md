# UX Copy

Write or review UX copy for any interface context.

## Input

Provide:
- **Context**: What screen, flow, or feature?
- **User state**: What is the user trying to do? How are they feeling?
- **Tone**: Formal, friendly, playful, reassuring?
- **Constraints**: Character limits, platform guidelines?

## Principles

1. **Clear**: Say exactly what you mean. No jargon, no ambiguity.
2. **Concise**: Fewest words that convey the full meaning.
3. **Consistent**: Same terms for the same things everywhere.
4. **Useful**: Every word helps the user accomplish their goal.
5. **Human**: Write like a helpful person, not a robot.

## Copy Patterns

### CTAs
- Start with a verb: "Start free trial", "Save changes", "Download report"
- Be specific: "Create account" not "Submit"
- Match the outcome to the label

### Error Messages
Structure: What happened + Why + How to fix
- "Payment declined. Your card was declined by your bank. Try a different card or contact your bank."

### Empty States
Structure: What this is + Why it's empty + How to start
- "No projects yet. Create your first project to start collaborating with your team."

### Confirmation Dialogs
- Make the action clear: "Delete 3 files?" not "Are you sure?"
- Describe consequences: "This can't be undone"
- Label buttons with the action: "Delete files" / "Keep files" not "OK" / "Cancel"

### Tooltips
- Concise, helpful, never obvious

### Loading States
- Set expectations, reduce anxiety

### Onboarding
- Progressive disclosure, one concept at a time

## Voice and Tone

Adapt tone to context:
- **Success**: Celebratory but not over the top
- **Error**: Empathetic and helpful
- **Warning**: Clear and actionable
- **Neutral**: Informative and concise

## Output Format

```markdown
## UX Copy: [Context]

### Recommended Copy
**[Element]**: [Copy]

### Alternatives
| Option | Copy | Tone | Best For |
|--------|------|------|----------|
| A | [Copy] | [Tone] | [When] |
| B | [Copy] | [Tone] | [When] |
| C | [Copy] | [Tone] | [When] |

### Rationale
[Why this copy works]

### Localization Notes
[Anything translators should know]
```

## With Knowledge Base MCP

If a knowledge base (Notion, Confluence) is connected:
- Pull brand voice guidelines and content style guide
- Check for existing copy patterns and terminology standards

## Tips

1. **Be specific about context** — "Error message when payment fails" beats "error message"
2. **Share brand voice** — "Professional but warm" helps match tone
3. **Consider emotional state** — Error messages need empathy; success can celebrate
