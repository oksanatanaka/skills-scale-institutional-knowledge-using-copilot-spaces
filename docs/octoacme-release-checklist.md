# OctoAcme Release Checklist

## Purpose
This consolidated checklist covers pre-release, deployment, and post-deploy validation steps. It harmonizes with the [Release & Deployment Guide](./octoacme-release-and-deployment.md) to ensure consistent, low-risk releases.

---

## Release Information

**Release Version:** [X.Y.Z]  
**Release Type:** Patch | Minor | Major  
**Target Date:** [YYYY-MM-DD]  
**Release Owner:** [Name]  
**On-Call Engineer:** [Name]

---

## Pre-Release Checklist

### Code Readiness
- [ ] All planned PRs merged to release branch
- [ ] No open blockers or critical bugs
- [ ] Code freeze in effect (if applicable)

### Quality Gates
- [ ] All acceptance criteria met for included features
- [ ] CI pipeline passing (tests, linting, build)
- [ ] Security scans completed and issues addressed
- [ ] Code coverage meets minimum threshold

### Testing
- [ ] Unit tests passing
- [ ] Integration tests passing
- [ ] End-to-end smoke tests passing
- [ ] Manual QA sign-off obtained
- [ ] Performance/load testing completed (if applicable)

### Documentation
- [ ] Release notes drafted and reviewed
- [ ] User-facing documentation updated
- [ ] API documentation updated (if applicable)
- [ ] Runbook/operational docs updated

### Risk & Rollback
- [ ] Rollback plan documented
- [ ] Rollback tested in staging (for major releases)
- [ ] Risk register reviewed for release-related risks
- [ ] On-call engineer identified and available

### Communication
- [ ] Stakeholders notified of release timing
- [ ] Support team briefed on changes
- [ ] Release announcement drafted

---

## Deployment Checklist

### Pre-Deployment
- [ ] Deployment window confirmed with stakeholders
- [ ] Backup/snapshot created (if applicable)
- [ ] Monitoring dashboards reviewed (baseline metrics)
- [ ] Alert thresholds verified

### Staging Deployment
- [ ] Deploy to staging environment
- [ ] Run smoke tests in staging
- [ ] Verify key user flows work correctly
- [ ] Check logs for errors or warnings
- [ ] Performance spot-check completed

### Production Deployment

#### Staged Rollout (Recommended)
- [ ] **Canary (1-5%):** Deploy to canary instances
  - [ ] Monitor for 15-30 minutes
  - [ ] Check error rates, latency, key metrics
  - [ ] Go/No-Go decision: ________
- [ ] **Percentage Rollout (25%):** Expand to 25% of traffic
  - [ ] Monitor for 30-60 minutes
  - [ ] Verify metrics stable
  - [ ] Go/No-Go decision: ________
- [ ] **Percentage Rollout (50%):** Expand to 50% of traffic
  - [ ] Monitor for 30-60 minutes
  - [ ] Go/No-Go decision: ________
- [ ] **Full Rollout (100%):** Complete deployment
  - [ ] Final verification complete

#### Direct Deployment (Lower-risk releases)
- [ ] Deploy to production
- [ ] Verify deployment successful
- [ ] Run production smoke tests

---

## Post-Deploy Validation

### Immediate Verification (0-30 minutes)
- [ ] Application is accessible and responsive
- [ ] Health check endpoints returning 200
- [ ] No spike in error rates
- [ ] Key user flows working (login, core features)
- [ ] Logs show no unexpected errors

### Monitoring Window (30 minutes - 4 hours)
- [ ] Error rates within acceptable thresholds
- [ ] Latency/performance metrics stable
- [ ] No increase in support tickets
- [ ] Synthetic monitoring passing
- [ ] Business metrics unaffected (if applicable)

### Post-Release Monitoring (4-24 hours)
- [ ] Continue monitoring key metrics
- [ ] Watch for delayed issues (caching, async jobs)
- [ ] Collect initial user feedback

---

## Go/No-Go Criteria

### Go Criteria
- All smoke tests pass
- Error rate < [X]% (define threshold)
- P99 latency < [Y]ms (define threshold)
- No critical alerts triggered
- Key user flows verified

### No-Go (Rollback) Criteria
- Critical functionality broken
- Error rate > [X]% sustained for 5+ minutes
- P99 latency > [Y]ms sustained
- Security vulnerability discovered
- Data integrity issues detected

---

## Rollback Procedure

### When to Rollback
- No-Go criteria met
- Critical customer impact reported
- Security or data integrity issue discovered

### Rollback Steps
1. [ ] Notify on-call and stakeholders
2. [ ] Trigger rollback to previous version
3. [ ] Verify rollback successful
4. [ ] Run smoke tests on rolled-back version
5. [ ] Confirm error rates returning to baseline
6. [ ] Document incident and trigger post-mortem

---

## Post-Release Tasks

### Communication
- [ ] Announce release to stakeholders
- [ ] Notify support team release is complete
- [ ] Update release notes with any last-minute changes
- [ ] Post to relevant channels (Slack, email)

### Documentation
- [ ] Close release milestone in project board
- [ ] Archive release branch (if applicable)
- [ ] Update project README with new version
- [ ] Document any known issues

### Follow-up
- [ ] Schedule release retrospective (if major release)
- [ ] Review action items from deployment
- [ ] Update runbooks based on learnings

---

## Release Sign-Off

| Role | Name | Sign-Off | Date |
|------|------|----------|------|
| Release Owner | | ☐ | |
| QA Lead | | ☐ | |
| Tech Lead | | ☐ | |
| PM/PdM | | ☐ | |

---

## Related Documentation
- [Release & Deployment Guide](./octoacme-release-and-deployment.md)
- [Risk Register Template](./octoacme-risk-register-template.md)
- [Weekly Status Template](./octoacme-weekly-status-template.md)
- [Retrospective & Continuous Improvement](./octoacme-retrospective-and-continuous-improvement.md)
