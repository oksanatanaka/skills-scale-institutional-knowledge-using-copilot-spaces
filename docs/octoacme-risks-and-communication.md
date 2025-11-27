# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register
Maintain a simple table with:
- ID
- Description
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Owner
- Mitigation plan
- Status

## Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduced via actions, contingency plans
- Monitor: review at weekly syncs and update status

## Stakeholder Communication
- Identify stakeholder groups and communication needs (e.g., engineering, sales, support)
- Provide regular updates (weekly or milestone-based)
- Use a single source of truth (project README or release doc) for status
- See [Project README Template](./octoacme-project-readme-template.md) for status documentation

### Stakeholder Update Frequency by Audience

| Audience | Frequency | Format | Content Focus |
|----------|-----------|--------|---------------|
| Executive Sponsor | Bi-weekly or milestone-based | Email summary or brief meeting | High-level status, key risks, decisions needed |
| Product Leadership | Weekly | Written status report | Progress vs. plan, blockers, scope changes |
| Engineering Team | Daily standups + weekly sync | Standup, project board | Technical progress, dependencies, blockers |
| Cross-functional Partners | Weekly or as needed | Email or Slack update | Integration points, timeline impacts |
| Support/CS Team | Pre-release + post-release | Training session + documentation | Feature overview, known issues, FAQs |
| End Users | Release-based | Release notes, changelog | New features, improvements, migration steps |

## Communication Templates

### Weekly Status Report
Use the [Weekly Status Template](./octoacme-weekly-status-template.md) for consistent status reporting.

**Quick Reference:**
- Progress this week:
- Next steps:
- Risks & blockers:
- Ask / decisions needed:

### Incident Communication
- Triage summary
- Actions being taken
- Expected timeline
- Post-incident blameless retrospective scheduled

## Escalation Paths
- Team-level -> PM -> Product Lead -> Sponsor
- For security incidents, follow the security incident runbook and notify Security on-call

### Escalation SLAs by Severity

| Severity | Definition | Initial Response | Escalation Timeline | Notification |
|----------|------------|------------------|---------------------|--------------|
| Critical (P0) | Production down, security breach, data loss | 15 minutes | Immediate to Sponsor | Page on-call, notify leadership |
| High (P1) | Major feature broken, significant customer impact | 1 hour | 4 hours to Product Lead | Slack + email to stakeholders |
| Medium (P2) | Feature degraded, workaround available | 4 hours | 24 hours to PM | Daily standup, weekly sync |
| Low (P3) | Minor issue, cosmetic, low impact | 24 hours | 1 week to PM | Track in backlog |

**Escalation Process:**
1. Identify severity level based on impact
2. Notify appropriate parties within initial response SLA
3. If unresolved within escalation timeline, escalate to next level
4. Document in Risk Register with status updates
5. Conduct post-incident review for P0/P1 issues

## Related Templates
- [Risk Register Template](./octoacme-risk-register-template.md)
- [Weekly Status Template](./octoacme-weekly-status-template.md)
- [Project README Template](./octoacme-project-readme-template.md)
