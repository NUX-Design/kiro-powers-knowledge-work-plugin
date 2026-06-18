# Structured Debugging

Run a systematic debugging session to find and fix issues.

## Workflow

```text
┌─────────────────────────────────────────────────────────────────┐
│                            DEBUG                                │
├─────────────────────────────────────────────────────────────────┤
│  Step 1: REPRODUCE                                              │
│  ✓ Expected vs actual behavior                                  │
│  ✓ Reproduction steps                                           │
│  ✓ Scope and impact                                             │
│                                                                 │
│  Step 2: ISOLATE                                                │
│  ✓ Narrow the component or code path                            │
│  ✓ Check recent deploys, config changes, dependencies           │
│  ✓ Review logs and error messages                               │
│                                                                 │
│  Step 3: DIAGNOSE                                               │
│  ✓ Form hypotheses and test them                                │
│  ✓ Trace the code path                                          │
│  ✓ Identify root cause, not just symptoms                       │
│                                                                 │
│  Step 4: FIX                                                    │
│  ✓ Propose a fix with rationale                                 │
│  ✓ Consider side effects and edge cases                         │
│  ✓ Suggest regression tests                                     │
└─────────────────────────────────────────────────────────────────┘
```

## Useful Inputs

- Exact error text or stack trace
- Steps to reproduce
- Recent changes
- Logs, screenshots, or metric symptoms
- Expected versus actual behavior

## Output

```markdown
## Debug Report: [Issue Summary]

### Reproduction
- **Expected**: [What should happen]
- **Actual**: [What happens instead]
- **Steps**: [How to reproduce]

### Root Cause
[Explanation of why the bug occurs]

### Fix
[Code changes or configuration fixes needed]

### Prevention
- [Test to add]
- [Guard to put in place]
```

## If Relevant MCP Tools Are Connected

- Pull logs, metrics, and deploy correlations from monitoring tools.
- Identify recent code changes from source control.
- Search for related bug reports or create a fix ticket in a project tracker.

## Tips

1. Preserve exact error wording.
2. Call out what changed recently.
3. Include environmental constraints such as only-in-prod or only-large-payloads.
