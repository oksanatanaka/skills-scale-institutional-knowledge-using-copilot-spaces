# OctoAcme Pull Request Description Template

## Purpose
This template ensures consistent, high-quality pull request descriptions that enforce traceability, quality gates, and risk awareness. Use this template for all PRs to maintain standards outlined in [Execution & Tracking](./octoacme-execution-and-tracking.md).

---

## PR Description Template

Copy the template below into your PR description:

```markdown
## Summary
<!-- Brief description of what this PR does and why -->

## Linked Issue
<!-- Required: Link to the issue this PR addresses -->
Closes #[issue_number]

## Type of Change
<!-- Check all that apply -->
- [ ] Bug fix (non-breaking change that fixes an issue)
- [ ] New feature (non-breaking change that adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to change)
- [ ] Documentation update
- [ ] Refactoring (no functional changes)
- [ ] Performance improvement
- [ ] Test coverage improvement

## Acceptance Criteria
<!-- Copy from the linked issue or define here -->
- [ ] [Criterion 1]
- [ ] [Criterion 2]
- [ ] [Criterion 3]

## Test Plan
<!-- Describe how you tested these changes -->

### Automated Tests
- [ ] Unit tests added/updated
- [ ] Integration tests added/updated
- [ ] All existing tests pass

### Manual Testing
<!-- Steps to manually verify the changes -->
1. [Step 1]
2. [Step 2]
3. [Expected result]

## Risk Assessment
<!-- Consider potential risks and rollback needs -->

### Risk Level
- [ ] Low — Isolated change, minimal impact
- [ ] Medium — Affects multiple components, reversible
- [ ] High — Wide impact, requires careful monitoring

### Rollback Plan
<!-- How to revert if issues are discovered -->
- Revert this PR: `git revert <commit_sha>`
- Additional steps (if any): [describe]

### Feature Flag
<!-- If applicable -->
- [ ] Behind feature flag: `[flag_name]`
- [ ] No feature flag needed

## Security Considerations
<!-- Check all that apply -->
- [ ] No security impact
- [ ] Reviewed for common vulnerabilities (XSS, SQL injection, etc.)
- [ ] Sensitive data handling reviewed
- [ ] Security team review requested (if applicable)

## Documentation
<!-- Check all that apply -->
- [ ] README updated (if applicable)
- [ ] API documentation updated (if applicable)
- [ ] No documentation changes needed

## Screenshots / Recordings
<!-- If applicable, add screenshots or recordings to show the changes -->

## Checklist
<!-- Ensure all items are complete before requesting review -->
- [ ] Code follows project style guidelines
- [ ] Self-review completed
- [ ] Tests pass locally
- [ ] CI checks pass
- [ ] Documentation updated (if needed)
- [ ] Linked to issue
- [ ] PR is appropriately sized (<= 400 lines preferred)

## Additional Notes
<!-- Any additional context for reviewers -->
```

---

## Guidelines for Effective PRs

### PR Size
- **Target:** ≤ 400 lines of changes when possible (additions + deletions combined)
- **Why:** Smaller PRs get faster, more thorough reviews
- **If larger:** Consider splitting into logical, incremental PRs

### Linking Issues
- **Required:** Every PR must link to at least one issue
- **Format:** Use `Closes #123` or `Fixes #123` to auto-close issues
- **Multiple issues:** List each on a separate line

### Acceptance Criteria
- Copy directly from the linked issue when available
- Each criterion should be independently verifiable
- Use checkboxes for tracking during review

### Test Plan
- Describe both automated and manual testing performed
- Include steps for reviewers to verify changes
- Note any areas that couldn't be fully tested

### Risk & Rollback
- Assess risk level honestly
- Document specific rollback steps
- Consider using feature flags for high-risk changes
- Link to [Risk Register](./octoacme-risk-register-template.md) if risk is discovered

---

## Review Expectations

### For Authors
- Respond to review comments within 1 business day
- Resolve or address all comments before merging
- Request re-review after significant changes

### For Reviewers
- Complete reviews within 1 business day
- Focus on correctness, security, and maintainability
- Approve when satisfied, even with minor nits

---

## Related Documentation
- [Execution & Tracking](./octoacme-execution-and-tracking.md)
- [Project Planning](./octoacme-project-planning.md)
- [Release & Deployment Guide](./octoacme-release-and-deployment.md)
- [Risk Register Template](./octoacme-risk-register-template.md)
