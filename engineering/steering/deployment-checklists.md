# Deployment Checklists

Generate a pre-deployment checklist to verify readiness before shipping.

## Output

```markdown
## Deploy Checklist: [Service/Release]
**Date:** [Date] | **Deployer:** [Name]

### Pre-Deploy
- [ ] All tests passing in CI
- [ ] Code reviewed and approved
- [ ] No known critical bugs in release
- [ ] Database migrations tested (if applicable)
- [ ] Feature flags configured (if applicable)
- [ ] Rollback plan documented
- [ ] On-call team notified

### Deploy
- [ ] Deploy to staging and verify
- [ ] Run smoke tests
- [ ] Deploy to production (canary if available)
- [ ] Monitor error rates and latency for 15 min
- [ ] Verify key user flows

### Post-Deploy
- [ ] Confirm metrics are nominal
- [ ] Update release notes / changelog
- [ ] Notify stakeholders
- [ ] Close related tickets

### Rollback Triggers
- Error rate exceeds [X]%
- P50 latency exceeds [X]ms
- [Critical user flow] fails
```

## Customization Inputs

- Feature flags in use
- Database migrations included
- Breaking API or schema changes
- Service-specific rollback constraints

## If Relevant MCP Tools Are Connected

- Pull release diffs and approval status from source control.
- Verify build and test state from CI/CD tooling.
- Pre-fill rollback thresholds from monitoring baselines.

## Tips

1. Use this before every deploy, not just risky ones.
2. Decide rollback criteria before starting the release.
3. Reuse a tailored checklist for recurring service patterns.
