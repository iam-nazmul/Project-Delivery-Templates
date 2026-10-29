# Spike / Feasibility — [Project name]

| Field | Entry |
| --- | --- |
| Project | [Project name] |
| Document | Spike / Feasibility |
| Version | [1.0] |
| Based on | BRD v[x.x], Gap Analysis v[x.x] |
| Date | [YYYY-MM-DD] |
| Author | [Name] |
| Status | Planned / Running / Complete |

**Workflow step:** 3. Spike / feasibility. **Next step:** 4. Development (Go) or back to 1. BRD (rework).

## 1. Verdict

**Guidance:** write this last. One sentence answer, then what is proven and what is not.

**[Feasible / Feasible with changes / Not feasible].** [One sentence why.]

- **Proven:** [ ]
- **Still unproven:** [ ]
- **BRD changes needed:** [ ]

## 2. Scope, timebox and test setup

- **Timebox:** [n] working days, [n] people. Stop when the go / no-go rules can be applied.
- **In the spike:** [what is built or tested]
- **Not in the spike:** [what is left for development]

**Test environment**

| ID | Machine / environment | Purpose |
| --- | --- | --- |
| E-1 | [ ] | [Recommended setup] |
| E-2 | [ ] | [Minimum setup] |

**Test data**

| ID | Data / sample | Why |
| --- | --- | --- |
| D-1 | [ ] | [Baseline] |
| D-2 | [ ] | [Hard case] |

## 3. Options and licence check

| Component | Option | Licence (checked [YYYY-MM-DD]) | Commercial use | Result |
| --- | --- | --- | --- | --- |
| [ ] | [ ] | [ ] | Yes / No | Chosen / excluded |

## 4. Experiments

**Guidance:** one row per question from the gap analysis. Each experiment names its fallback, so a failure leads to a decision rather than a debate.

| # | Experiment | Pass condition | If it fails | Result |
| --- | --- | --- | --- | --- |
| X1 | [End-to-end run] | [Measurable] | **Rework** to step 1 | |
| X2 | [Quality of option A vs B] | [Score ≥ n] | [Use option B / fallback] | |
| X3 | [Performance] | [Time ≤ n] | [Reduce scope / raise hardware] | |
| X4 | [ ] | [ ] | [ ] | |

## 5. Prototype

| Item | Description |
| --- | --- |
| Code location | [Repository / folder] |
| What it does | [ ] |
| How to run | [Steps or command] |
| What was tested | [ ] |
| Known limits | [ ] |

## 6. Go / no-go rules

| Outcome | Decision |
| --- | --- |
| All "rework" experiments pass | **Go** to step 4, Development |
| A "rework" experiment fails after one tuning retry | **Rework:** back to step 1 (see Rework Plan) |
| Only experiments with a fallback fail | Go, with the fallback written into the BRD |
| 2 rework loops on the same experiment | Product owner decides: reduced release or not feasible |

## 7. Re-spike for change requests

**Guidance:** used when UAT feedback or a change request needs a new technical approach (see Feedback and Change Management).

1. **Scope:** change request ID, component, evidence that triggered it.
2. **Timebox:** [3] days per component; [5] if adding a new tool or model.
3. **Candidates:** at most 3, each checked for licence and constraints before testing.
4. **Experiment:** reuse the matching experiment above, plus the case where the problem appeared.
5. **Pass:** meets the original pass condition **and** fixes the reported problem; no regression in the end-to-end and performance experiments.

**Re-spike log**

| Change request | Date | Component | Candidates | Winner | Results | Decision |
| --- | --- | --- | --- | --- | --- | --- |
| | | | | | | |

## 8. Sources

- [Link to licence page, documentation or benchmark used]

## 9. Change log

| Version | Date | Change |
| --- | --- | --- |
| 1.0 | [YYYY-MM-DD] | First version |
