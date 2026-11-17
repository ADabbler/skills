# Lifecycle and Retention

## Review criteria

For each affected note, decide what remains useful, where it belongs, and whether its status matches reality. Remove spent process text from active notes.

## States

| Directory | Admission criteria |
| --- | --- |
| `proposed` | Investigation, planning, implementation, or deferred work |
| `implemented` | Adopted, required acceptance checks complete, and still useful for maintenance |
| `rejected` | Unadopted, with rejection rationale that still prevents a plausible mistake |
| `archived` | Previously implemented, with historical value but no current guiding role |

Blocking acceptance gaps keep a note in `proposed`. Explicitly accepted nonblocking verification gaps may remain in `implemented`; acceptance requirements follow the agreed scope.

## Transitions

| Situation | Action |
| --- | --- |
| Backfill an existing decision | Record a verified decision directly in `implemented`; identify unknown historical motives as unknown |
| Finish an investigation | Develop a proposal if work continues; otherwise keep findings in a related note only when they help future work, and prune spent material. Research completion alone is not implementation |
| Complete a proposal | Move to `implemented`, rewrite as current behavior, remove execution checklists and resolved findings, and retain useful evidence, limits, and coverage gaps |
| Defer work | Keep in `proposed`, stating why and when to reconsider |
| Reject or abandon | Move to `rejected` if the rationale prevents recurrence; otherwise prune |
| Facts change, decision holds | Update paths, names, and other facts in place |
| Revise a proposal under discussion | Update the proposal in place to reflect current choices and rationale |
| Replace an effective decision or its decisive rationale | Create a new proposal and cross-link it with the current note; the existing decision remains current until its replacement takes effect |
| Partial supersession | Narrow the old note to still-valid decisions and rationale, linking both notes |
| Full supersession | Retain content still needed by current work in related active notes; archive the old note when its independent historical value warrants preservation, otherwise prune |
| Complete consolidation | Preserve every unique useful proposition, then remove the redundant record |
| Revisit a rejection | Create a proposal citing the rejection and identify which premises changed |
| Reintroduce an archived approach | Create a current Agent Note citing the historical evidence |

Move topic directories as a group. On completion, fold retained nonblocking findings into the main note and remove spent supporting material. When moving or deleting a note, update references to it in current project files. Links about current behavior should point to the current explanation; historical citations within Agent Notes may point to the archive. Repair relative links within moved active notes.

## Retention

Judge retention by usefulness for future work.

During active work, findings, progress, and open questions may be worth retaining for task continuity alone. At completion, retain conclusions in related notes as needed for future work, and clear material whose working purpose has ended. Project documentation describes the current implementation; historical context may remain in notes when worth retaining.

Before consolidating, archiving, or pruning a note, account for its still-relevant decisions, rationale, applicability conditions, ownership rules, negative guarantees, evidence, coverage gaps, and reintroduction conditions. Keep content that still guides current work in relevant active notes, with its sources and verification scope.

Mechanical records, complete duplicates, and rejections that no longer prevent plausible mistakes can be pruned.

## Archiving

Archive implemented decisions only when they no longer guide current work and retain independent historical value. Preserve `Status: implemented`, add `Archived: YYYY-MM-DD`, and move the record with its evidence. Keep the archived body and evidence unchanged.

Archives are excluded from default retrieval. Correct discovered factual errors in a current Agent Note citing the historical snapshot. Explicit cleanup may delete archives that have lost their value.
