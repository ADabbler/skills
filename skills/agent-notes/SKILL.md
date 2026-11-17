---
name: agent-notes
description: Create and maintain project working notes and decision records. Use for task continuity and handoff, and to review, consolidate, prune, or archive related notes as work progresses, at task completion, or when decisions change.
---

# Agent Notes

Keep only the project context another session needs to resume work or understand a decision without the authoring conversation. Organize notes around a concrete topic and keep them current.

## Decide what to record

Read applicable project instructions and Notes conventions, and locate the existing Notes directory before creating files. Scope the work to the user's task. Reviews report findings; authorized maintenance applies changes.

Record notes when requested or when preserving context helps continue, review, or hand off the work. Search related notes and project documentation first. Update the relevant note as work on the same topic progresses. Create a note when none fits; use a separate record when replacing an effective decision or its decisive rationale. Capture lasting rationale or constraints not explained by code, tests, or documentation. Mechanical edits and obvious local fixes do not by themselves warrant a standalone note.

When notes and code disagree, establish whether the note is stale, implementation violates the agreed decision, or the decision changed. Correct the appropriate source using evidence.

## Resume the work

At the start of related work, search active notes for the goal, agreed scope, constraints, findings, current progress, blockers, and next step. Verify changeable facts against implementation and evidence. Consult archives for historical questions. From the existing Notes directory, use a search such as:

```sh
rg --hidden --no-ignore --glob '!archived/**' 'mechanism-or-topic' .
```

Update the relevant note after meaningful findings or progress and before handoff. Keep facts, hypotheses, pending choices, and confirmed decisions distinguishable. Replace outdated working context rather than accumulating a session log, and link relevant files and evidence.

At task completion, when adding or replacing a decision, or when evidence changes a recorded premise, review notes affected by the task without waiting for a separate cleanup request.

## Paths and content

Use the project's existing Notes directory, or `.agents/notes/` under the project root.

- Use `proposed/`, `implemented/`, `rejected/`, and `archived/`; create a directory only when a record belongs there.
- Start flat. Add one level of stable classification when retrieval needs justify it, and use consistent category names across lifecycles.
- Name notes `YYYY-MM-DD-topic.md` with a short English topic and the original proposal date. Preserve that date through edits and moves. For backfilled decisions with an unknown original date, use the recording date and identify it as such.
- Prefer one file. When separate review or evidence is useful, use a dated topic directory containing `index.md`, with `review.md` and `evidence/` as needed. Record the group's status in `index.md`.
- Write notes in the language requested by the user, otherwise the conversation language. Directory names and status values use English.
- A `README.md` at the Notes root, when useful, records project-specific conventions and entry points. Follow the project's choice of version-control tracking.

Read the [writing guide](references/writing-guide.md) when creating, restructuring, or reviewing a note. Read [calibration examples](references/examples.md) when creation or retention value is unclear.

## Maintain and review

Read the [lifecycle rules](references/lifecycle.md) when reviewing affected notes, choosing or changing status, superseding records, consolidating, pruning, or archiving. Recording a proposal does not authorize implementation. Moves, deletion, and external verification follow the task's permissions; report any pending action that requires additional authorization.

Check facts, status, paths, recorded alternatives, and relevant coverage or verification gaps. Public documentation and required build workflows must remain usable without private notes.

After edits, briefly report changes, unresolved issues, and checks actually run. Distinguish static checks from behavioral verification.

For editorial work, use `prose-standard` when available.
