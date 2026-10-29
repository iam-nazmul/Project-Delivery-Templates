# Release Approval — [Project name]

| Field | Entry |
| --- | --- |
| Project | [Project name] |
| Document | Release Approval |
| Version | [1.0] |
| Release candidate | [version / build hash] |
| Meeting date | [YYYY-MM-DD] |
| Chair | [Product owner] |

**Workflow gate:** 6. UAT → 7. Deployment ("Approved"). Only the exact approved build is deployed.

## 1. Approval criteria

All items ticked = **Approved**. Open items with an agreed fix plan = **Approved with conditions**.

**Quality (Test Plan)**

- [ ] All test cases run; [95]%+ pass; every Must-requirement case passes
- [ ] Zero open critical defects; at most [n] major with workarounds
- [ ] Security, privacy and performance tests pass

**Users (UAT Plan)**

- [ ] All UAT scenarios pass
- [ ] Ratings at or above pass averages

**Changes (Feedback and Change Management)**

- [ ] Every CR is Verified, Deferred or Rejected
- [ ] User-facing CRs passed their UAT re-check

**Compliance**

- [ ] Licences and attributions checked
- [ ] Release notes, user guide and support material complete

## 2. Evidence pack

Shared at least [2] working days before the meeting.

| Item | Owner |
| --- | --- |
| Final test report and open defect list | QA lead |
| UAT report and sign-off record | Product owner |
| Change register | Product owner |
| Build version, hash and checksums | Lead developer |
| Licence and attribution list | Lead developer |
| Release notes | Product owner |
| Deployment and rollback plan | Lead developer |
| Support readiness | Support lead |

## 3. Approvers and decisions

| Approver | Confirms | Can block? |
| --- | --- | --- |
| Product owner (final decision) | Business value, UAT result, accepted risks | Yes |
| QA lead | Test results meet criteria | Yes |
| Lead developer | Build is the tested one; deployment ready | Yes |
| Support lead | Users can get help | No (raises a condition) |

| Decision | Next step |
| --- | --- |
| Approved | Release freeze, then step 7, Deployment |
| Approved with conditions | Conditions fixed and verified by a set date, then deploy |
| Not approved | Change requests raised; fix sprint or re-spike; new meeting |

A condition may never cover a critical defect or a security, privacy or licence problem.

## 4. Go / no-go meeting

**Agenda (45 min):** release candidate scope → QA results → UAT results → change register → deployment and support readiness → each approver's go / no-go → decision and record.

**Rules:** decide on the evidence pack only; mark each criterion Met / Not met / Condition; write down accepted risks; share the record the same day.

## 5. After approval

- Tag the approved build (for example `v1.0.0`); record checksums.
- Freeze: any later change is a new CR, new build and, unless class A, a new approval.

| Condition | CR | Owner | Due | Verified by | Status |
| --- | --- | --- | --- | --- | --- |
| | | | | | |

**Handoff to Deployment:** record signed; build and checksums handed over; release notes final; date and rollback owner agreed; support briefed.

## 6. Approval record

| Field | Entry |
| --- | --- |
| Release version and build hash | |
| Quality / Users / Changes / Compliance criteria | Met / Not met / Condition |
| Open defects accepted | |
| CRs deferred | |
| Risks accepted, with reasons | |
| Conditions | |
| Decision | Approved / Approved with conditions / Not approved |
| Product owner signature and date | |
| QA lead signature and date | |
| Lead developer signature and date | |

## 7. Change log

| Version | Date | Change |
| --- | --- | --- |
| 1.0 | [YYYY-MM-DD] | First version |
