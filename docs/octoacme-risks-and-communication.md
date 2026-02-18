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

## Communication Templates
Weekly Status Template:
- Progress this week:
- Next steps:
- Risks & blockers:
- Ask / decisions needed:

Incident Communication
- Triage summary
- Actions being taken
- Expected timeline
- Post-incident blameless retrospective scheduled

## Incident Response Workflow

### Security Incidents
When a security vulnerability or breach is discovered:

1. **Immediate Response** (within 15 minutes):
   - Notify Security on-call via designated channel
   - Assess severity (Critical, High, Medium, Low)
   - Initiate incident response team if Critical/High

2. **Triage** (within 1 hour):
   - Security Engineer confirms impact and scope
   - Determine containment strategy
   - Notify PM and Product Lead
   - Create incident ticket with timeline

3. **Containment & Mitigation**:
   - Security Engineer leads remediation
   - Developers implement fixes
   - QA validates fix in staging
   - Security Engineer approves deployment

4. **Communication**:
   - Hourly updates to stakeholders for Critical incidents
   - Daily updates for High severity
   - Use incident communication template
   - Notify affected customers if data exposure occurred

5. **Post-Incident**:
   - Blameless retrospective within 3 business days
   - Document root cause and lessons learned
   - Create action items to prevent recurrence
   - Update security runbooks

### Production Incidents
For non-security production issues:

1. **Detection & Response**:
   - Monitor alerts trigger incident
   - On-call engineer assesses impact
   - Create incident ticket and notify PM

2. **Triage & Resolution**:
   - Determine if rollback or fix-forward
   - Implement solution
   - Validate in production
   - Monitor for recurrence

3. **Post-Incident Review**:
   - Hold retrospective within 1 week
   - Capture lessons learned
   - Identify process improvements
   - Update runbooks and monitoring

## Escalation Paths
- Team-level -> PM -> Product Lead -> Sponsor
- For security incidents, follow the security incident runbook and notify Security on-call
