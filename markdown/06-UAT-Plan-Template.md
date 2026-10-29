# User Acceptance Testing (UAT) Plan — [Project name]

| Field | Entry |
| --- | --- |
| Project | [Project name] |
| Document | UAT Plan |
| Version | [1.0] |
| Based on | BRD v[x.x], Test Plan v[x.x] |
| Release candidate | [version] |
| Date | [YYYY-MM-DD] |
| Author | [Product owner / UAT lead] |

**Workflow step:** 6. UAT. **Next step:** 7. Deployment (Approved) or 3. Spike (Feedback / changes).

## 1. Entry criteria

- [ ] QA exit criteria met; test report approved
- [ ] Release candidate available to testers
- [ ] Zero open critical defects
- [ ] Quick-start guide ready
- [ ] Testers recruited; sessions booked; feedback form ready

## 2. Objectives, scope and participants

QA proves the product works as specified; UAT checks that real users find it useful and acceptable.

**Objectives**

1. [Users can complete their main tasks without help]
2. [The output is good enough for real use]
3. [It works in users' real environments]

**Participants**

| Group | Number | Profile | Why |
| --- | --- | --- | --- |
| [User group] | [n] | [ ] | [ ] |
| **Total** | **[n]** | | |

## 3. Setup and session format

| Session | Format | Length |
| --- | --- | --- |
| 1. Setup | [Install / access, introduction] | [ ] |
| 2. Guided tasks | Tester does scenarios while a facilitator observes without helping | [ ] |
| 3. Real use | Tester uses the product alone in their own setting | [ ] |
| 4. Debrief | Feedback form plus interview | [ ] |

## 4. UAT scenarios

**Guidance:** give testers the task in plain words, never the steps. A scenario passes when [80]% of testers complete it without help.

| ID | Task given to the tester | Accepted when | Covers |
| --- | --- | --- | --- |
| UAT-01 | "[Task in user language]" | [ ] | BR-xx |
| UAT-02 | "[ ]" | [ ] | BR-xx |

## 5. Feedback form

| # | Question (1 = very poor, 5 = excellent) | Pass (average) |
| --- | --- | --- |
| F1 | [ ] | [n] |
| F2 | [ ] | [n] |
| F3 | How easy was it to use? | [n] |

**Open questions:** best part; what almost stopped you; would you use it instead of [current solution]; would you recommend it (0–10).

## 6. Handling feedback

| Route | CR class | When | Next step |
| --- | --- | --- | --- |
| Fix in UAT | Bug / A | Small fix | Fix build, QA verifies, tester re-checks |
| BRD update | B | A limit or priority must change | BRD, Development, QA |
| Back to step 3, Spike | C | Needs a new technical approach | Re-spike, Development, QA, UAT re-check |
| BRD fallback | E | A known fallback exists | Apply; update release notes |
| Later version | D / F | New feature or wish | Backlog |

## 7. UAT re-check for changes

| CR class | Re-check | How |
| --- | --- | --- |
| A (user-facing) | Optional | Reporting tester confirms |
| B (user-facing) | Yes | [3] testers repeat affected scenarios |
| C | Yes | [5] testers repeat affected scenarios and ratings |
| E | No | QA confirms |

## 8. Acceptance criteria and schedule

**UAT is approved when:**

- [ ] All scenarios pass ([80]%+ without help)
- [ ] Ratings meet their pass averages
- [ ] Zero open critical issues; major issues fixed or accepted
- [ ] All user-facing changes passed their re-check

| Days | Activity |
| --- | --- |
| [ ] | Setup sessions |
| [ ] | Guided tasks |
| [ ] | Real use |
| [ ] | Debriefs and analysis |
| [ ] | Final fixes, report, sign-off |

## 9. Outcomes and sign-off

| Decision | Meaning |
| --- | --- |
| Approved | Moves to step 7, Deployment |
| Approved with conditions | Deploy after listed fixes are verified |
| Not approved | Change requests raised; fix sprint or re-spike; UAT re-check |

| Field | Entry |
| --- | --- |
| Release candidate | |
| UAT dates | |
| Testers | |
| Scenario pass rate | |
| Average ratings | |
| Change requests raised / verified / deferred | |
| Decision | Approved / Approved with conditions / Not approved |
| Product owner signature and date | |
| QA lead signature and date | |

## 10. Change log

| Version | Date | Change |
| --- | --- | --- |
| 1.0 | [YYYY-MM-DD] | First version |
