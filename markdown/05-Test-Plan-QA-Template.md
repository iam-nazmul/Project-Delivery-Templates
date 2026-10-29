# Test Plan (QA) — [Project name]

| Field | Entry |
| --- | --- |
| Project | [Project name] |
| Document | Test Plan (QA) |
| Version | [1.0] |
| Based on | BRD v[x.x], Development Plan v[x.x] |
| Build under test | [version / build hash] |
| Date | [YYYY-MM-DD] |
| Author | [QA lead] |

**Workflow step:** 5. Testing (QA). **Next step:** 6. UAT.

## 1. Entry criteria

- [ ] All Must requirements merged to `main`
- [ ] Release-candidate build available for all target platforms
- [ ] Release notes and known issues provided
- [ ] Test data ready
- [ ] Open bugs: none critical, at most [n] major

## 2. Scope and approach

**In scope:** [requirement IDs]. **Out of scope:** [items and reason].

| Test type | What it checks | How |
| --- | --- | --- |
| Functional | Each acceptance condition | Manual / automated test cases |
| Regression | Nothing broke between builds | Automated suite |
| Performance | [Speed, load, resource use] | [Tool / timed runs] |
| Security / privacy | [Data, access, network] | [ ] |
| Compatibility | [OS, browsers, devices] | Test matrix |
| Installation / upgrade | [Install, upgrade, uninstall] | Clean environments |
| Robustness | Error handling and fallbacks | Fault injection |

## 3. Test environments and data

| ID | Environment | Purpose |
| --- | --- | --- |
| ENV-1 | [ ] | [Recommended] |
| ENV-2 | [ ] | [Minimum] |

| ID | Test data | Used for |
| --- | --- | --- |
| DATA-1 | [ ] | [ ] |

## 4. Functional test cases

| ID | Requirement | Steps | Expected result | Result | Defect |
| --- | --- | --- | --- | --- | --- |
| TC-01 | BR-01 | [ ] | [ ] | Pass / Fail | |
| TC-02 | BR-02 | [ ] | [ ] | | |

## 5. Non-functional test cases

| ID | Requirement | Test | Pass condition | Result |
| --- | --- | --- | --- | --- |
| NT-01 | NFR-01 | [ ] | [ ] | |
| NT-02 | NFR-02 | [ ] | [ ] | |

## 6. Quality review (if output quality needs human judgement)

**Reviewers:** [n] people from [target user group], not on the project team.

| Criterion | Question | Pass (average, 1–5) |
| --- | --- | --- |
| [ ] | [ ] | [n] |

## 7. Defect management

| Severity | Definition | Fix target |
| --- | --- | --- |
| Critical | Crash, data loss, security/privacy failure, or a Must requirement fails | Before next build |
| Major | Should requirement fails, or quality below pass | Within the test cycle |
| Minor | Works with a workaround; small visual issue | Before release if time allows |
| Trivial | Cosmetic | Backlog |

**Each defect records:** build, environment, test case, steps, expected vs actual, logs.

**Workflow:** New → Triaged → Fixed → Closed / Reopened. A defect that needs a requirement or technology change becomes a change request.

## 8. Testing change requests

| CR class | QA tests | Regression |
| --- | --- | --- |
| A. Minor | Affected cases | Related UI / unit tests |
| B. Requirement tweak | Updated cases | Automated suite |
| C. New technical approach | All cases for the component, plus performance and security | Full regression |
| D. New feature | New cases | Full regression |
| E. Fallback | Fallback works; scope matches release notes | Automated suite |

CR test cases are named `TC-CRxxx-nn`. QA marks a CR **Verified** only after its cases pass.

## 9. Schedule and reporting

| Week | Activity |
| --- | --- |
| 1 | [Installation, functional tests] |
| 2 | [Non-functional, quality review, fixes] |
| 3 | [Re-tests, full regression, report] |

**Reporting:** daily status (run, passed, failed, open defects by severity) and a final test report.

## 10. Exit criteria to UAT

- [ ] 100% of test cases run; [95]%+ pass; all Must-requirement cases pass
- [ ] Zero open critical defects; at most [n] open major defects with workarounds
- [ ] Performance and security tests pass
- [ ] Final test report approved by the product owner

**If not met:** another fix cycle of up to [1] week; a failure from a real limit becomes a change request.

## 11. Change log

| Version | Date | Change |
| --- | --- | --- |
| 1.0 | [YYYY-MM-DD] | First version |
