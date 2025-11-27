# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows

### Board Policies
Use the project board (e.g., GitHub Projects) with the following columns and policies:

| Column | Definition | WIP Limit |
|--------|------------|-----------|
| Backlog | Prioritized work not yet started | No limit |
| Ready | Items with clear acceptance criteria, estimated, and ready to pull | 10 items |
| In Progress | Actively being worked on by a team member | 2 per developer |
| In Review | PR opened and awaiting code review | 3 items |
| QA | Code merged to staging, awaiting QA validation | 5 items |
| Done | Accepted and ready for release | No limit |

**Definition of Ready:**
- [ ] Acceptance criteria clearly defined
- [ ] Estimated (story points or T-shirt size)
- [ ] Dependencies identified and resolved (or tracked in Risk Register)
- [ ] Design/technical approach agreed upon
- [ ] No blocking questions

**Definition of QA:**
- [ ] Code merged to staging environment
- [ ] Unit and integration tests passing
- [ ] Ready for manual acceptance testing
- [ ] Test scenarios documented or in acceptance criteria

### Pull Request Workflow
- **PR Size Guidance:**
  - Target: ≤ 400 lines of changes
  - If larger, split into logical incremental PRs
  - Exception: Large refactors may exceed limit with reviewer agreement
- Include issue link and acceptance criteria in PR description
- Use the [PR Description Template](./octoacme-pr-description-template.md) for consistency
- Run automated tests and linting in CI before requesting review
- Require at least one approval before merging (or team-defined policy)
- **Risk Linking:** When a risk is discovered during implementation, add it to the [Risk Register](./octoacme-risk-register-template.md) and reference it in the PR

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly (see [Risk Register Template](./octoacme-risk-register-template.md))
- [ ] WIP limits configured on project board
- [ ] Definition of Ready posted and understood by team

## Related Templates
- [PR Description Template](./octoacme-pr-description-template.md)
- [Risk Register Template](./octoacme-risk-register-template.md)
- [Weekly Status Template](./octoacme-weekly-status-template.md)
- [Project README Template](./octoacme-project-readme-template.md)
