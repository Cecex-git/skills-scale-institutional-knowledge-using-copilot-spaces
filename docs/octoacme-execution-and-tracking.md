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

### QA Handoff Process
Clear handoff to QA ensures quality and prevents miscommunication:

1. **Entry Criteria**: Before moving to QA column:
   - All acceptance criteria implemented
   - Unit and integration tests passing
   - Code review approved and merged
   - Developer has completed smoke testing
   - Test environment updated with latest code

2. **Handoff**: Developer notifies QA with:
   - Link to feature/issue with acceptance criteria
   - Test scenarios to validate
   - Known limitations or edge cases
   - Environment/data setup instructions

3. **QA Validation**: QA Specialist:
   - Reviews acceptance criteria
   - Executes test plan
   - Documents any defects found
   - Verifies fixes when developer addresses issues

4. **Exit Criteria**: QA approves when:
   - All acceptance criteria validated
   - No critical or high-priority defects
   - Exploratory testing completed
   - Documentation updated if needed

5. **Sign-off**: QA moves item to Done and notifies PM

### Cross-Team Coordination
When work depends on or impacts other teams:

1. **Early Notification**: PM notifies dependent teams when:
   - Planning starts (to confirm availability)
   - Timelines change (to allow re-planning)
   - Blockers emerge (to coordinate resolution)

2. **Integration Checkpoints**: Schedule sync meetings:
   - Initial alignment on contracts/interfaces
   - Mid-development integration review
   - Pre-release integration testing

3. **Status Sharing**: Provide weekly updates including:
   - Progress on items dependent teams are waiting for
   - Any delays or scope changes
   - Upcoming needs or asks

4. **Escalation Process**:
   - Team-level: Developers coordinate directly
   - PM-level: PMs align on timeline and scope adjustments
   - Product Lead level: Strategic re-prioritization if needed
   - Sponsor level: Executive decision for resource allocation

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

### Security Review Integration
Security is integrated throughout development:

1. **Design Phase**: 
   - Conduct threat modeling for features handling sensitive data or authentication
   - Security Engineer reviews architecture for security concerns
   - Document security requirements and controls

2. **Development Phase**:
   - Automated security scanning runs in CI/CD pipeline
   - Developers address security warnings before requesting code review
   - Security-critical changes require Security Engineer review

3. **Security Scan Triage**:
   - Weekly review of security scan findings
   - Security Engineer prioritizes findings (Critical, High, Medium, Low)
   - Critical and High findings block release
   - Medium and Low findings tracked for future remediation

4. **Security Approval**:
   - Security Engineer approves releases with:
     - No open Critical or High severity findings
     - Acceptable risk for Medium findings with mitigation plan
     - Security documentation updated

5. **Security Incident Response**:
   - Security on-call notified immediately for production security issues
   - Follow incident response process (see Risk Management & Communication guide)
   - Post-incident review conducted with Security team

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
Clear escalation paths ensure blockers are resolved quickly:

**Level 1 - Team (resolve in < 1 day)**
- Developer-to-developer collaboration
- Triage in daily standup
- PM facilitates if cross-functional coordination needed

**Level 2 - PM/Product Lead (resolve in 1-3 days)**
- PM escalates to Product Lead for:
  - Scope or priority conflicts
  - Resource constraints
  - Dependencies on other teams
- Product Lead coordinates with dependent team leads
- Decision documented and communicated to team

**Level 3 - Sponsor (business-critical, resolve ASAP)**
- Escalate to Sponsor when:
  - Timeline impact affects business commitments
  - Resource allocation requires executive decision
  - Strategic trade-offs needed
- Sponsor authorizes resources or adjusts scope
- Executive decision communicated to all stakeholders

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
