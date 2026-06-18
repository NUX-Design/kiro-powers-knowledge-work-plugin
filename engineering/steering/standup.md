# Engineering Standups

Generate a standup update by pulling together recent activity across your tools or from notes you provide directly.

## How It Works

```text
┌─────────────────────────────────────────────────────────────────┐
│                           STANDUP                               │
├─────────────────────────────────────────────────────────────────┤
│  STANDALONE                                                     │
│  ✓ Structure rough notes into yesterday / today / blockers      │
│  ✓ Keep updates concise and action-oriented                     │
├─────────────────────────────────────────────────────────────────┤
│  WITH MCP TOOLS                                                 │
│  + Source control: recent commits and PRs                       │
│  + Project tracking: ticket movement                            │
│  + Chat: relevant discussions and decisions                     │
│  + CI/CD: build and deploy status                               │
└─────────────────────────────────────────────────────────────────┘
```

## Inputs

- Minimal: ask for a standup update.
- Better: provide rough notes about what you finished, what is next, and where you are blocked.

## Output

```markdown
## Standup — [Date]

### Yesterday
- [Completed item with ticket reference if available]

### Today
- [Planned item with ticket reference]

### Blockers
- [Blocker with context and who can help]
```

## If Relevant MCP Tools Are Connected

- Pull recent commits and PRs from source control.
- Summarize ticket movement from a project tracker.
- Surface chat discussions that matter for the update.
- Include CI/CD status when it affects priorities.

## Tips

1. Run this every morning to avoid reconstructing yesterday from memory.
2. Add blockers and priority context after the first draft.
3. Reformat for Slack, email, or your team template when needed.
