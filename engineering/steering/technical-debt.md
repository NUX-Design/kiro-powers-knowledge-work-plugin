# Technical Debt Management

Systematically identify, categorize, and prioritize technical debt.

## Categories

| Type | Examples | Risk |
|------|----------|------|
| **Code debt** | Duplicated logic, poor abstractions, magic numbers | Bugs, slow development |
| **Architecture debt** | Monolith pressure, wrong data store, brittle boundaries | Scaling limits |
| **Test debt** | Low coverage, flaky tests, missing integration tests | Regressions ship |
| **Dependency debt** | Outdated or unmaintained libraries | Security vulnerabilities |
| **Documentation debt** | Missing runbooks, stale READMEs, tribal knowledge | Onboarding pain |
| **Infrastructure debt** | Manual deploys, no monitoring, no infrastructure as code | Incidents, slow recovery |

## Prioritization Framework

Score each item on:

- Impact: how much it slows the team down, from 1 to 5
- Risk: what happens if it stays unresolved, from 1 to 5
- Effort: how hard the fix is, from 1 to 5, inverted for prioritization

Priority formula:

```text
(Impact + Risk) x (6 - Effort)
```

## Output

Produce:

- a prioritized debt list
- estimated effort
- business justification
- a phased remediation plan that can run alongside feature work
