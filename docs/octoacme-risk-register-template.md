# OctoAcme Risk Register Template

## Purpose
This template provides a ready-to-use risk register for tracking, assessing, and mitigating project risks. It aligns with the [Risk Management & Communication](./octoacme-risks-and-communication.md) documentation.

---

## Risk Register

**Project:** [Project Name]  
**Last Updated:** [YYYY-MM-DD]  
**Owner:** [PM Name]

---

### Active Risks

| ID | Risk Description | Category | Impact | Likelihood | Risk Score | Owner | Mitigation Plan | Status | Date Identified | Target Resolution |
|----|------------------|----------|--------|------------|------------|-------|-----------------|--------|-----------------|-------------------|
| R001 | [Example: Key team member may leave mid-project] | Resource | High | Medium | 6 | [Name] | Cross-train team members; document knowledge | Open | YYYY-MM-DD | YYYY-MM-DD |
| R002 | [Example: Third-party API may have breaking changes] | Technical | Medium | Medium | 4 | [Name] | Monitor API changelog; implement adapter pattern | Mitigating | YYYY-MM-DD | YYYY-MM-DD |
| R003 | [Example: Stakeholder requirements may change] | Scope | High | Low | 3 | [Name] | Weekly stakeholder sync; document decisions | Monitoring | YYYY-MM-DD | YYYY-MM-DD |

---

### Risk Scoring Matrix

Use this matrix to calculate Risk Score (Impact × Likelihood):

|              | **Low (1)** | **Medium (2)** | **High (3)** |
|--------------|-------------|----------------|--------------|
| **High (3)** | 3           | 6              | 9            |
| **Medium (2)** | 2         | 4              | 6            |
| **Low (1)**  | 1           | 2              | 3            |

**Risk Score Interpretation:**
- **7-9 (Critical):** Immediate action required; escalate to sponsor
- **4-6 (High):** Active mitigation needed; review weekly
- **2-3 (Medium):** Monitor closely; review bi-weekly
- **1 (Low):** Accept and monitor; review monthly

---

### Risk Categories

| Category | Description |
|----------|-------------|
| Technical | Technology, architecture, or implementation risks |
| Resource | Team capacity, skills, or availability risks |
| Scope | Requirements clarity, changes, or creep |
| Schedule | Timeline, dependencies, or deadline risks |
| External | Third-party, vendor, or regulatory risks |
| Security | Data protection, compliance, or vulnerability risks |

---

### Risk Status Definitions

| Status | Description |
|--------|-------------|
| Open | Risk identified but not yet addressed |
| Mitigating | Active mitigation efforts underway |
| Monitoring | Mitigation in place; monitoring for changes |
| Closed | Risk resolved or no longer applicable |
| Escalated | Raised to sponsor/leadership for decision |

---

### Closed/Resolved Risks

| ID | Risk Description | Resolution | Date Closed |
|----|------------------|------------|-------------|
| R000 | [Example: Initial infrastructure setup delayed] | Infrastructure provisioned ahead of schedule | YYYY-MM-DD |

---

### Escalation Thresholds

Risks should be escalated based on the following criteria:

| Condition | Escalation Path |
|-----------|-----------------|
| Risk Score ≥ 7 | Immediate PM → Product Lead → Sponsor |
| No progress on mitigation for 2 weeks | PM → Product Lead |
| Risk impacts other projects/teams | PM → Cross-team sync |
| Security-related risk | PM → Security Team (follow your organization's security incident runbook) |

---

### Weekly Review Checklist

- [ ] Review all Open and Mitigating risks
- [ ] Update status and mitigation progress
- [ ] Identify any new risks from execution
- [ ] Escalate Critical risks as needed
- [ ] Archive Closed risks

---

## Related Documentation
- [Risk Management & Communication](./octoacme-risks-and-communication.md)
- [Project README Template](./octoacme-project-readme-template.md)
- [Weekly Status Template](./octoacme-weekly-status-template.md)
- [Execution & Tracking](./octoacme-execution-and-tracking.md)
