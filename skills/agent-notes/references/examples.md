# Calibration Examples

Use these cases to judge the value of a note or passage. The deciding factor is what the information helps someone continue or decide.

## Recording working context and rationale

| Situation | Criterion and action |
| --- | --- |
| Two candidate libraries have been compared, but license compatibility remains unresolved | Keep the comparison, sources, open question, and next check in `proposed` |
| Implementation is interrupted after some checks pass | Update current progress, remaining checks, blockers, and relevant file links so work can resume |
| Fix a local condition with an obvious regression test | No additional durable rationale: no standalone note |
| A completed task has a long investigation log and one still-useful constraint | Keep the constraint, its reason and evidence in the relevant note; remove the resolved exploration and completed checklist |
| Choose an export encoding to satisfy the receiving system's documented requirements | Small change, non-obvious constraint: record the requirement and its source in a relevant existing note or create one if needed |
| Run each integration test in a separate process to isolate global state, increasing test time | Record the isolation requirement and runtime cost so future test optimizations preserve the required separation |
| Cancelling a background task leaves temporary files that another component must remove | Record who requests cancellation, who removes the files, and when cleanup is complete |

## Retaining useful conclusions

| Situation | Criterion and action |
| --- | --- |
| An investigation rules out a suspected dependency defect and identifies a supported configuration | If the finding helps future work, keep it and supporting evidence in a relevant note; clear spent investigation material |
| The storage approach changes, but the old note also contains backup requirements that still apply | Update or create the relevant decision note as needed, preserving backup requirements that still constrain the system |
| A completed decision no longer guides current work, but its historical tradeoff remains independently useful | Archive it during the affected-topic completion review; preserve its body and repair active inbound links |
| A comparison rejects one library on a still-relevant constraint | Keep the comparison in the chosen design's note; create a separate rejection only if it prevents recurring debate independently |
| A two-year-old rejection explains that retrying a timed-out payment can charge twice because the endpoint lacks idempotency support | Keep the rejection while that limitation applies; it still prevents a plausible mistake |
| That endpoint now supports idempotency keys, and the adopted retry design covers the remaining constraints | The rejection's premise is obsolete and its useful content is covered by current records; prune it |
