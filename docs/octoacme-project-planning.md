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

## Backlog Item Template
- Title:
- Description:
- Acceptance criteria:
- Priority:
- Estimate:
- Owner:
- Related docs/links:

## Sprint / Iteration Planning
- Timebox planning to agreed sprint length
- Pull items that meet DoD and have clear acceptance criteria
- Ensure team capacity is respected

## Risk & Dependency Management
- Capture in Risk Register:
  - ID, Description, Impact, Probability, Owner, Mitigation
- Mark cross-team dependencies in the project board and escalate during weekly syncs

### Cross-Team Dependency Management
Dependencies on other teams require proactive coordination:

1. **Identification**: During planning, identify all dependencies on other teams
2. **Documentation**: Create dependency items with:
   - Dependent team name and primary contact
   - What is needed and by when
   - Impact if dependency is not met
   - Alternative approaches if available
3. **Notification**: PM contacts dependent team leads to:
   - Confirm availability and timeline
   - Align on deliverables and acceptance criteria
   - Establish communication channel
4. **Tracking**: Add dependencies to project board with:
   - "Blocked" label when waiting
   - Regular status updates in weekly syncs
   - Escalation to Product Lead if timeline slips
5. **Integration Planning**: Define integration points:
   - API contracts or interface definitions
   - Test data and environments needed
   - Integration testing approach and ownership

### Dependency Communication Template
When reaching out to dependent teams:
```
Subject: Dependency Request for [Project Name]

Team: [Dependent Team Name]
Project: [Your Project Name]
Timeline: [When needed]

We need: [Clear description of dependency]
Context: [Why this is needed, business impact]
Success criteria: [What "done" looks like]
Point of contact: [Your team's contact]

Can we schedule 30 minutes to align on timeline and deliverables?
```

## Planning Checklist
- [ ] Project kickoff held
- [ ] Backlog prioritized and estimated
- [ ] Release timeline and milestones agreed
- [ ] Definition of Done documented
- [ ] Initial test plan / QA approach drafted
