# Code Review

Review code changes with a structured lens on security, performance, correctness, and maintainability.

## Suggested Inputs

- A PR URL
- A diff
- A file path
- A specific concern such as security, data integrity, or hot-path performance

If no code target is provided, ask what should be reviewed.

## Review Dimensions

### Security

- SQL injection, XSS, CSRF
- Authentication and authorization flaws
- Secrets or credentials in code
- Insecure deserialization
- Path traversal
- SSRF

### Performance

- N+1 queries
- Unnecessary memory allocations
- Algorithmic complexity in hot paths
- Missing database indexes
- Unbounded queries or loops
- Resource leaks

### Correctness

- Edge cases such as empty input, nulls, and overflow
- Race conditions and concurrency issues
- Error handling and propagation
- Off-by-one errors
- Type safety

### Maintainability

- Naming clarity
- Single responsibility
- Duplication
- Test coverage
- Documentation for non-obvious logic

## Output

```markdown
## Code Review: [PR title or file]

### Summary
[1-2 sentence overview of the changes and overall quality]

### Critical Issues
| # | File | Line | Issue | Severity |
|---|------|------|-------|----------|
| 1 | [file] | [line] | [description] | 🔴 Critical |

### Suggestions
| # | File | Line | Suggestion | Category |
|---|------|------|------------|----------|
| 1 | [file] | [line] | [description] | Performance |

### What Looks Good
- [Positive observations]

### Verdict
[Approve / Request Changes / Needs Discussion]
```

## If Relevant MCP Tools Are Connected

- Pull PR diffs automatically from source control.
- Check CI status and test results.
- Cross-reference linked tickets from a project tracker.
- Compare changes against team standards from a knowledge base.

## Tips

1. Provide context such as hot path, PII handling, or migration risk.
2. Narrow the lens when needed, for example security-only or performance-only.
3. Include tests in scope so coverage quality is reviewed too.
