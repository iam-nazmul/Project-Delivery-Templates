# Deployment Plan — [Project name]

| Field | Entry |
| --- | --- |
| Project | [Project name] |
| Document | Deployment Plan |
| Version | [1.0] |
| Release | [version] |
| Based on | Release Approval record of [YYYY-MM-DD] |
| Deployment owner | [Name] |
| Rollback owner | [Name] |

**Workflow step:** 7. Deployment. **Next step:** 8. Project closure.

## 1. Entry criteria

- [ ] Approval record signed (Approved, or all conditions verified)
- [ ] Approved build and checksums handed over
- [ ] Release notes and user guides final
- [ ] Deployment date and rollback owner agreed
- [ ] Support briefed
- [ ] Infrastructure / hosting ready and checked

## 2. What is released and where

| Artifact | Platform / environment | Notes |
| --- | --- | --- |
| [Installer / package / container / service] | [ ] | [Signed? Checksum?] |

| Channel | Use | Notes |
| --- | --- | --- |
| [Website / app store / server / internal portal] | [ ] | [ ] |

## 3. Dependencies and data

**Guidance:** list anything the release needs besides the build: databases, migrations, external services, large files, licences, keys.

| Dependency | Action before release | Owner |
| --- | --- | --- |
| [ ] | [ ] | [ ] |

## 4. Rollout plan

| Stage | Who | Duration | Move on when |
| --- | --- | --- | --- |
| 1. Early access / pilot | [Group, size] | [ ] | [No critical issues; success rate ≥ n%] |
| 2. Full release | [Everyone] | — | — |

**Runbook (day 0 = first release)**

| Day | Task | Owner |
| --- | --- | --- |
| −7 | [Prepare infrastructure / upload dependencies] | [ ] |
| −3 | [Smoke test in production-like environment] | QA |
| −1 | [Final go / no-go; support rota confirmed] | Product owner |
| 0 | [Release stage 1] | [ ] |
| 0–[n] | [Daily review of issues] | [ ] |
| [n] | [Stage review: continue, hotfix or roll back] | [ ] |
| [n+1] | [Full release and announcement] | [ ] |

**Smoke test:** [the short list of checks run after each deployment].

## 5. Rollback plan

**Roll back when:** [critical defect affecting many users, data loss, security problem].

1. Product owner decides; deployment owner acts within [2] hours.
2. [Restore previous version / stop downloads / switch traffic]
3. [Restore data if needed]
4. Notify users and the team.
5. Fix through a hotfix CR, QA verification and short approval.
6. Record the incident in the change register.

## 6. After release

**Monitoring**

| Signal | Source | Watched for |
| --- | --- | --- |
| [Errors / uptime / downloads / support requests] | [ ] | [ ] |

**Support:** channels [ ], reply target [ ], FAQ location [ ].

**Hotfixes:** critical defects fixed within [n] working days through a CR; other issues go to the backlog.

## 7. Deployment sign-off and handoff

**Deployment is complete when:**

- [ ] Full release live for [14] days
- [ ] No open critical defect
- [ ] Support within its reply target
- [ ] Figures collected for closure

| Field | Entry |
| --- | --- |
| Released version(s) and dates | |
| Pilot users and issues found | |
| Usage figures after [n] days | |
| Hotfixes / rollbacks | |
| Open issues handed on | |
| Product owner and deployment owner sign-off | |

## 8. Change log

| Version | Date | Change |
| --- | --- | --- |
| 1.0 | [YYYY-MM-DD] | First version |
