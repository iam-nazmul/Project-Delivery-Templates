# Rework Plan — Spike Not Feasible — [Project name]

| Field | Entry |
| --- | --- |
| Project | [Project name] |
| Document | Rework Plan |
| Version | [1.0] |
| Based on | Spike / Feasibility v[x.x] |
| Date | [YYYY-MM-DD] |
| Author | [Name] |

**Workflow loop:** 3. Spike → 1. BRD ("Not feasible / rework").

## 1. When this applies

Rework starts when a spike experiment fails and no fallback covers it.

| Failed experiment | Rework? | Why |
| --- | --- | --- |
| [X1 end-to-end] | Yes | [Core promise not proven] |
| [X2] | Yes / No | [ ] |
| [X3] | No — use fallback | [ ] |

## 2. Rework process

**Guidance:** one rework loop should take no more than [5] working days before the spike re-runs.

1. **Record the failure** with the rework record below: experiment, result, data, environment.
2. **Find the cause:** a tuning problem (fixable inside the spike) or a real limit of the chosen approach.
3. **Retry once if it is tuning.** If the retry passes, continue to development without rework.
4. **Choose a rework option** with the product owner (playbook below).
5. **Update the BRD (step 1):** change the affected requirement, priority or target; new BRD version.
6. **Update the gap analysis (step 2)** for the changed requirements only.
7. **Re-run the spike (step 3)** for the failed experiments, plus the end-to-end experiment.
8. **Limit loops:** after 2 loops on the same experiment, the product owner decides between further rework and "not feasible".

## 3. Failure playbook

| Failure | Likely cause | Tuning fix (retry once) | Rework option | BRD change |
| --- | --- | --- | --- | --- |
| [X1] | [ ] | [ ] | [Replace component] | [ ] |
| [X2] | [ ] | [ ] | [Alternative approach] | [Lower priority / relax target] |
| [X3] | [ ] | [ ] | [Reduce scope] | [Move to later version] |

## 4. Not feasible: when to stop

The product owner declares the project not feasible when, after the rework loops:

- [The core experiment still fails]
- [Two key experiments both fail]
- [The only working option breaks a fixed constraint: cost, licence, regulation, hardware]

**When stopping, record:** final results, the blocking component, what would need to change, a review date, and any reusable parts.

**Alternative to stopping:** a reduced release — [describe smallest useful scope] — if the product owner accepts it.

## 5. Rework record (one per loop)

| Field | Entry |
| --- | --- |
| Rework loop # | |
| Date | |
| Failed experiment(s) | |
| Result vs pass condition | |
| Data and environment | |
| Cause (tuning or limit) | |
| Tuning retry result | |
| Rework option chosen | |
| BRD changes (ID, old → new) | |
| BRD new version | |
| Approved by | |
| Re-spike result | |
| Decision | Go / rework again / not feasible |

## 6. Change log

| Version | Date | Change |
| --- | --- | --- |
| 1.0 | [YYYY-MM-DD] | First version |
