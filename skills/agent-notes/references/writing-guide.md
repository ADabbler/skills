# Note Writing Guide

Write for the next person resuming the task or revisiting the decision. Use the shortest form that preserves what they need. Choose headings and order for the actual subject; a simple note may need only a status line and a few paragraphs, while a complex plan may use sections by problem, component, or execution sequence. No section or alternative count is required unless the project specifies one.

## Basic information

A main note identifies its topic and lifecycle status:

```markdown
# <Topic>

Status: proposed
```

Use `proposed`, `implemented`, or `rejected` according to the [lifecycle rules](lifecycle.md). An archived note retains `Status: implemented` and adds `Archived: YYYY-MM-DD`. The filename or topic directory carries the original proposal date, or a clearly identified recording date when backfilling a decision with an unknown original date; `Archived` records when archival occurred.

## Write for the record's purpose

One note may combine findings, a proposal, and review results. Keep each fact with its explanation and link to existing background instead of repeating it. Select only the guidance relevant to the work; these categories are not a template to fill.

### Investigation

State the question, scope, and evidence needed to conclude the investigation. Distinguish verified findings, hypotheses, and open questions; keep sources near the claims they support. Preserve the current position, completed checks, blockers, relevant files, and next useful step where they help resume work. Summarize evidence rather than pasting search output or exploration transcripts.

### Proposal

Explain a problem that stands independently of the proposed solution. State the concrete choice, deciding reasons, meaningful costs and risks, and observable completion conditions. Distinguish approved decisions from pending choices. Keep current progress and the next step when useful.

Include alternatives actually considered when the comparison helps explain the choice. Give their strongest relevant argument and the reason for choosing or rejecting them. Omit the section when there are none; do not invent options.

### Implemented

Explain the problem solved and the current decision, mechanism, scope, and non-obvious rationale. Retain benefits, costs, limits, relevant alternatives, evidence, accepted nonblocking coverage or verification gaps, and reconsideration conditions where they guide maintenance. Keep essential behavior local and link extended implementation details to relevant source files or documentation.

### Rejected

Identify the proposal, deciding objection, and conditions that make it unsuitable. Include a current alternative or reconsideration condition when known and useful for preventing repeated debate.

### Review

Each unresolved finding states the defect, location, impact, and evidence. Make recommendations actionable. A short paragraph is usually enough. Fold still-useful conclusions and evidence into the relevant body text before removing resolved findings.

## Evidence

Summarize what was checked, how, the result, and uncovered scope; include version or environment when it affects interpretation. Link durable evidence and summarize temporary evidence. Distinguish completed checks from planned or pending checks, and identify source inspection, simulation, or live execution as the evidence method. Do not repeat the same result under progress, acceptance, and verification headings.

## Short investigation note

This fictional example shows a compact handoff.

```markdown
# Export failure investigation

Status: proposed

Goal: establish whether a failed export can damage an existing file, covering both single and batch exports.

Confirmed: writeExport in src/export.ts opens the destination before validating all fields. In a local reproduction, a single export with an invalid field failed and left an existing destination empty.

Open question: does batch export use the same write path? Only single export has been reproduced.

Next step: inspect src/batch-export.ts, then determine where validation should happen.
```

The source location and observed result support the finding; the open question limits its scope. The goal and next step let another session resume the investigation. A few paragraphs are enough for this record.
