# OctoAcme — Project Planning

## Purpose
Turn an approved initiative into an actionable plan and backlog for delivery.

## Objectives
- Break work into shippable increments
- Identify dependencies and risks
- Align timelines, releases, and responsibilities

## Activities
1. Kickoff meeting with stakeholders and delivery team
2. Create prioritized backlog with acceptance criteria
3. Estimate scope (T-shirt sizing or story points)
4. Define Definition of Done (DoD)
5. Identify dependencies and integration points
6. Create release plan and milestone map
7. Define test strategy per backlog item

## Definition of Done (DoD) Examples
A backlog item is "Done" when:
- [ ] Code complete and merged to main branch
- [ ] Unit tests written and passing (minimum 80% coverage for new code)
- [ ] Integration tests added for cross-component functionality
- [ ] Documentation updated (README, API docs, inline comments as needed)
- [ ] Observability in place (logging, metrics, alerts configured)
- [ ] Security review completed (for sensitive features)
- [ ] Accessibility requirements met (for UI changes)
- [ ] Code review approved by at least one team member
- [ ] QA acceptance testing passed
- [ ] No open critical or high-severity bugs

## Backlog Item Template
- Title:
- Description:
- Acceptance criteria:
- Priority:
- Estimate:
- Owner:
- Related docs/links:
- Test strategy:

## Test Strategy Per Backlog Item
Each backlog item should include a lightweight test strategy that covers:

| Test Type | Required? | Description |
|-----------|-----------|-------------|
| Unit Tests | Yes | Test individual functions/methods in isolation |
| Integration Tests | When applicable | Test interactions between components or services |
| E2E Tests | For critical paths | Validate end-to-end user flows |
| Manual QA | For user-facing changes | Exploratory testing and acceptance verification |
| Performance Tests | For performance-sensitive changes | Load/stress testing if applicable |

**Test Strategy Template for Backlog Items:**
```
## Test Strategy
- [ ] Unit tests: [describe scope]
- [ ] Integration tests: [describe scope or N/A]
- [ ] E2E tests: [describe critical paths or N/A]
- [ ] Manual QA: [describe test scenarios]
- [ ] Performance: [describe approach or N/A]
```

## Sprint / Iteration Planning
- Timebox planning to agreed sprint length
- Pull items that meet DoD and have clear acceptance criteria
- Ensure team capacity is respected

## Risk & Dependency Management
- Capture in Risk Register:
  - ID, Description, Impact, Probability, Owner, Mitigation
- Mark cross-team dependencies in the project board and escalate during weekly syncs

## Planning Checklist
- [ ] Project kickoff held
- [ ] Backlog prioritized and estimated
- [ ] Release timeline and milestones agreed
- [ ] Definition of Done documented
- [ ] Initial test plan / QA approach drafted
- [ ] Test strategy defined for each backlog item
- [ ] Risk Register initialized (see [Risk Register Template](./octoacme-risk-register-template.md))

## Related Templates
- [Project README Template](./octoacme-project-readme-template.md)
- [Risk Register Template](./octoacme-risk-register-template.md)
- [Weekly Status Template](./octoacme-weekly-status-template.md)
