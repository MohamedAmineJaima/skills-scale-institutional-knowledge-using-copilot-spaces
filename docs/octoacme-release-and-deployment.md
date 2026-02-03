# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted (Product Manager with technical input from Developers)
- Rollback / mitigation plan documented (Developers with Project Manager)
- Smoke tests prepared (QA Lead)
- Final QA sign-off obtained (QA Lead)
- UX review completed for UI changes (UX Designer)
- Success metrics instrumentation verified (Data Analyst)
- Stakeholder communication prepared (Product Manager)

## Deployment Checklist
- [ ] Deployment window scheduled (if needed) (Project Manager)
- [ ] Backup or snapshot (if applicable) (Developers)
- [ ] Deploy to staging and run smoke tests (QA Lead validates)
- [ ] Final UX review in staging environment (UX Designer)
- [ ] Deploy to production (automated pipeline preferred) (Developers)
- [ ] Run post-deploy verifications (QA Lead and Developers)
- [ ] Verify analytics tracking is working (Data Analyst)
- [ ] Monitor dashboards for errors or anomalies (Data Analyst and Developers)
- [ ] Announce release to stakeholders and support (Product Manager and Project Manager)

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call (Project Manager)
  - QA Lead validates issue severity and impact
  - Rollback to last known-good release if necessary (Developers)
  - Data Analyst monitors metrics to confirm rollback success
  - Triage root cause and capture action items (full team)
  - Business Analyst documents impact for stakeholders

## Role Involvement in Release

- **QA Lead**: Final testing sign-off, smoke testing, post-deployment validation
- **Developers**: Code deployment, rollback procedures, post-deployment monitoring
- **UX Designer**: Final UX review in staging, validate UI in production
- **Data Analyst**: Verify tracking works, monitor metrics post-release, identify anomalies
- **Product Manager**: Release notes, stakeholder communication, go/no-go decision
- **Project Manager**: Coordinate release activities, manage deployment window, incident escalation
- **Business Analyst**: Document release impact, support user communication if needed
- **Scrum Master**: Facilitate release retrospective to capture learnings

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
