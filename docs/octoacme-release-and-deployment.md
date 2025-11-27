# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support

For a comprehensive checklist, use the [Release Checklist Template](./octoacme-release-checklist.md).

## Staged Rollout Guidance
For production deployments, use a staged rollout approach to minimize risk:

### Canary Deployment (Recommended for all releases)
1. **Canary (1-5% of traffic)**
   - Deploy to a small subset of instances
   - Monitor for 15-30 minutes
   - Watch error rates, latency, and key business metrics
   - Go/No-Go decision before proceeding

2. **Percentage-Based Rollout**
   - 25% → Monitor 30-60 minutes → Go/No-Go
   - 50% → Monitor 30-60 minutes → Go/No-Go
   - 100% → Full deployment

### When to Use Staged Rollout
| Release Type | Rollout Strategy |
|--------------|------------------|
| Patch (hotfix) | Direct deploy (if critical) or quick canary |
| Minor release | Canary → 25% → 50% → 100% |
| Major release | Extended canary → 10% → 25% → 50% → 100% |
| Breaking changes | Feature flag + staged rollout |

### Rollout Monitoring Thresholds
- **Error rate increase:** > 0.1% above baseline → pause rollout
- **Latency increase:** > 10% P99 above baseline → pause rollout
- **Failed health checks:** Any → immediate investigation

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Post-Release Monitoring Window
After deployment, maintain a monitoring window to catch delayed issues:

### Monitoring Window Timeline
| Phase | Duration | Focus | Actions |
|-------|----------|-------|---------|
| Immediate | 0-30 min | Critical failures | Active monitoring, ready to rollback |
| Short-term | 30 min - 4 hours | Performance, errors | Check dashboards, error rates, latency |
| Extended | 4-24 hours | Edge cases, async issues | Monitor queues, batch jobs, user reports |
| Long-term | 24-72 hours | Business impact | Verify metrics, collect feedback |

### Go/No-Go Criteria
**Go (Continue with release):**
- All smoke tests pass
- Error rate within 0.1% of baseline
- P99 latency within 10% of baseline
- No critical alerts triggered
- Key user flows verified working

**No-Go (Rollback required):**
- Critical functionality broken
- Error rate > 1% above baseline for 5+ minutes
- P99 latency > 25% above baseline
- Security vulnerability discovered post-deploy
- Data integrity issues detected

### Post-Release Verification Checklist
- [ ] Health check endpoints returning 200
- [ ] Key user flows working (test in production)
- [ ] Logs show no unexpected errors
- [ ] Synthetic monitoring passing
- [ ] No spike in support tickets
- [ ] Business metrics unaffected

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:

## Related Templates
- [Release Checklist](./octoacme-release-checklist.md)
- [Risk Register Template](./octoacme-risk-register-template.md)
- [Weekly Status Template](./octoacme-weekly-status-template.md)
- [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md)
