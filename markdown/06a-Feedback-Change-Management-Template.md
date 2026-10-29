# Feedback and Change Management — [Project name]

| Field | Entry |
| --- | --- |
| Project | [Project name] |
| Document | Feedback and Change Management |
| Version | [1.0] |
| Date | [YYYY-MM-DD] |
| Owner | [Product owner] |

**Workflow loop:** 6. UAT → 3. Spike ("Feedback / changes"), and any change request during the project.

## 1. Sources of feedback and change

| Source | Typical content | Collected by |
| --- | --- | --- |
| UAT testers | Ratings, interviews, issues | UAT facilitator |
| QA | Defects that need a requirement change | QA lead |
| Product owner | New business needs, priorities | Product owner |
| Development | Technical limits, dependency changes | Lead developer |
| Released users | Support requests, reviews | Support |

Code-only bugs follow the Test Plan's defect workflow. This process covers **changes** to requirements, scope, priority, technology or schedule.

## 2. Change process

1. **Capture:** log a change request (CR) with the template below; group related feedback into one CR.
2. **Triage (within [2] working days):** check clarity, merge duplicates, set urgency.
3. **Classify and route:** choose the class and the step it returns to.
4. **Impact analysis:** fill the checklist.
5. **Decide:** approve, reject or defer, following the approval rules.
6. **Update documents:** BRD first, then each affected document, with new versions.
7. **Implement and verify:** through its route; QA verifies; UAT re-checks user-facing changes.
8. **Close:** mark Closed and tell the requester.

**Statuses:** New → Triaged → Analysing → Approved / Rejected / Deferred → In progress → Verified → Closed.

## 3. Classification and routing

| Class | Description | Goes back to | Then |
| --- | --- | --- | --- |
| A. Minor | UI wording, layout, defaults; no requirement change | Step 4, Development | QA re-test |
| B. Requirement tweak | Changes a target, priority or limit; same technology | Step 1, BRD | Development, QA |
| C. New technical approach | Current component cannot meet the need | **Step 3, Spike** | Gap analysis, Development, QA, UAT re-check |
| D. New feature / scope | Adds a requirement | Step 1, BRD | Full flow (spike if risky) |
| E. Fallback | Known limit with an agreed fallback | Product owner decision | Release notes; QA confirms |
| F. Deferred | Valid but not for this version | Backlog | Next planning |

## 4. Impact analysis and approval

**Checklist (classes B, C, D)**

- [ ] Requirements affected and new acceptance conditions
- [ ] Modules affected
- [ ] Effort and release-date impact
- [ ] Licence, security, privacy and compliance impact
- [ ] Performance and infrastructure impact
- [ ] Test cases to add or change; UAT re-check needed?
- [ ] Risk of doing it, and of not doing it

**Approval rules**

| Change | Approver |
| --- | --- |
| Class A under [2] days | Lead developer (product owner informed) |
| Class B, or under [5] days | Product owner |
| Class C or D, date change, or licence/security/privacy impact | Change board: product owner, lead developer, QA lead |

During UAT and deployment, classes A, B and E go into the current release; class C only if it blocks approval; others are deferred.

## 5. Documents to update

| Document | A | B | C | D | E |
| --- | --- | --- | --- | --- | --- |
| BRD | — | Yes | Yes | Yes | Yes |
| Gap Analysis | — | If feasibility changes | Yes | Yes | — |
| Spike / Feasibility | — | — | Yes | If risky | — |
| Development Plan | If a module changes | Yes | Yes | Yes | If scope moves |
| Test Plan | Affected cases | Yes | Yes | Yes | Yes |
| UAT Plan | — | If user-facing | Yes | Yes | — |
| Release notes | Yes | Yes | Yes | Yes | Yes |

## 6. Change request template

| Field | Entry |
| --- | --- |
| CR ID | CR-[nnn] |
| Date raised | |
| Raised by / source | |
| Title | |
| Description and reason | |
| Evidence | |
| Requirements affected | |
| Class | A / B / C / D / E / F |
| Routes back to step | |
| Impact summary | |
| Decision, by whom, date | |
| Documents updated | |
| Verified in build / test case | |
| Status | |

## 7. Change register

| CR | Date | Title | Source | Class | Route | Decision | Status |
| --- | --- | --- | --- | --- | --- | --- | --- |
| | | | | | | | |

## 8. Change log

| Version | Date | Change |
| --- | --- | --- |
| 1.0 | [YYYY-MM-DD] | First version |
