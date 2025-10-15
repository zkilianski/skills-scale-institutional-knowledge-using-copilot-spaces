# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

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
- [ ] Risk register updated weekly

## Cross-Role Coordination During Execution

### Development to UX Designer Handoffs
- UX Designer provides design specs and assets before development starts
- Developer reviews designs and asks clarifying questions early
- UX Designer reviews implementation and provides feedback during PR review
- Designer validates final implementation in staging environment

### Development to Data Analyst Handoffs
- Data Analyst defines tracking requirements and event specifications
- Developer implements tracking according to specifications
- Data Analyst validates tracking in development/staging environment
- Analyst confirms data accuracy before production release

### Development to Security Handoffs
- Security Lead reviews design for security concerns during planning
- Developer follows secure coding guidelines and runs security scans
- Security Lead reviews high-risk changes and PRs involving auth/data
- Security scan results reviewed before merge and release

### QA to Development Handoffs
- Clear acceptance criteria defined in tickets before development
- Developer tests locally and documents testing approach
- QA reviews and tests according to acceptance criteria
- QA reports issues with clear reproduction steps; developer fixes and re-tests

### Development to Release Manager Handoffs
- Developer ensures all tests pass and PRs are merged to release branch
- Developer provides release notes content and migration steps if needed
- Release Manager coordinates deployment timing with developer on-call availability
- Developer validates deployment in production and monitors for issues

### Customer Support Integration
- Support Lead informed of upcoming changes during weekly sync
- Support documentation updated before release goes live
- Support Lead escalates customer-reported bugs to developers with priority
- Post-release: Support Lead provides feedback on customer reception

### Daily Execution Touchpoints by Role
- **Developers**: Daily standup, PR reviews, pair programming as needed
- **UX Designer**: Design reviews, implementation check-ins, usability validation
- **Data Analyst**: Data validation, dashboard updates, ad-hoc analysis
- **QA/Testing**: Test execution, bug triage, acceptance validation
- **Project Manager**: Standup facilitation, blocker resolution, status tracking
- **Security Lead**: Security scan monitoring, vulnerability triage (as needed)
- **Release Manager**: Release readiness tracking, deployment coordination (near release)
- **Customer Support Lead**: Customer feedback review, escalation management (as needed)

## Cross-Role Handoff Checklist Template

Use this checklist when work transitions between roles to ensure nothing is missed:

### Feature/Story Handoff Checklist

**From Product Manager to UX Designer:**
- [ ] User story with problem statement provided
- [ ] Success metrics and acceptance criteria defined
- [ ] Target users and use cases identified
- [ ] Constraints and requirements documented

**From UX Designer to Developers:**
- [ ] Design specifications and mockups provided
- [ ] Interactive prototype available (if needed)
- [ ] Accessibility requirements documented
- [ ] Design assets exported and shared
- [ ] Edge cases and error states designed

**From Developers to QA/Testing:**
- [ ] Feature implemented per acceptance criteria
- [ ] Unit tests written and passing
- [ ] Test data and scenarios documented
- [ ] Known limitations or issues noted
- [ ] Local testing completed

**From QA/Testing to Release Manager:**
- [ ] All acceptance criteria validated
- [ ] Regression testing completed
- [ ] Smoke test scenarios documented
- [ ] Known issues logged and prioritized
- [ ] Release notes input provided

**From Release Manager to Customer Support:**
- [ ] Release date and changes communicated
- [ ] Support documentation updated
- [ ] Training or demo provided (if needed)
- [ ] Known issues and workarounds shared
- [ ] Escalation contacts identified

**Data Analyst Integration Points:**
- [ ] Tracking requirements shared before development
- [ ] Analytics implementation validated in staging
- [ ] Success metrics dashboard prepared
- [ ] Baseline metrics documented pre-release

**Security Lead Integration Points:**
- [ ] Security requirements reviewed during planning
- [ ] Threat model reviewed (for sensitive features)
- [ ] Security scans passed before merge
- [ ] Vulnerability findings addressed
- [ ] Security sign-off obtained before release
