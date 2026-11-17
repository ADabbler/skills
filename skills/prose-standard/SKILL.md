---
name: prose-standard
description: Use when writing, reviewing, restoring, trimming, or auditing technical prose in project and API documentation, decision records, code and test comments, prompts, descriptions, diagnostics, and CLI/UI text. Also use when deciding where documentation or comments are needed. Improve clarity and completeness while preserving factual meaning.
---

# Prose Standard

Preserve the facts readers need to act or maintain the system. Remove repetition and narration about the writing session that adds no understanding.

## Scope

Determine audience, purpose, and file scope from the request and context. Proceed when these are clear. Reviews report findings; authorized editing tasks apply changes.

## Preserve necessary propositions

Before rewriting, identify actor and action, conditions, timing, obligation or permission, exceptions, failures, ownership, and consequences. Retain facts relevant to the reader's task.

State essential behavior and limits at the point of use. Link to existing explanations of architecture, algorithms, extended rationale, or examples instead of repeating them. A link cannot replace a failure condition the caller needs locally. Prefer a short paragraph over separate sections that repeat the same fact.

Explain non-obvious rationale when omission could cause misuse or an incorrect simplification. In code comments, let code and types express operations already clear at that location.

## Check coverage as well as wording

Judge completeness by what the intended reader needs to understand or do. User documentation supplies the necessary information without requiring source inspection. Add or restore missing information during authorized edits; report it during reviews. Accurate existing sentences alone do not establish completeness.

| Location | Necessary information to check |
| --- | --- |
| Project READMEs | Purpose, intended users, a usable starting point, essential requirements and limitations, and links to detailed guidance |
| Configuration references | Supported values, defaults, precedence, when changes take effect, and consequences of invalid settings |
| Architecture and design explanations | Current structure, responsibilities, important interactions, rationale, tradeoffs, and constraints that guide maintenance |
| Public interface documentation | Return distinctions, failure conditions, side effects, and relevant ownership, cancellation, completion, or durability guarantees |
| Task guides | Prerequisites, actual operations, observable success, and recovery from likely failures |
| Internal comments | Non-obvious invariants, ownership, and ordering that affect safe maintenance |
| Test comments | Why a special fixture, indirect observation, or platform accommodation is necessary |
| Decision and working records | Current decision or open question, non-obvious rationale, and evidence or limits needed to resume or revisit it |
| Diagnostics | Failing subject or input, cause or violated condition, and corrective action where useful |

Use these criteria where the facts matter to the reader and are not already clear locally. They are coverage prompts, not required sections. Choose the amount of explanation for the task; do not fill templates with routine background, exhaustive inventories, or invented content.

## Write from the reader's perspective

- Follow explicit language requirements for the text. Otherwise, preserve the language of existing or surrounding material. For new material without that context, use project conventions, or the conversation language if none apply.
- Current-state documents describe current behavior. Decision and historical records may retain useful background or alternatives. Proposals preserve uncertainty, postmortems preserve causal sequence, and frozen snapshots follow their preservation rules.
- Replace stale descriptions in place.
- Prefer concrete actors and actions. Keep technical terms when they identify the actual subject.
- Organize explanations around the reader's task: provide needed context before dependent steps, and place exceptions beside the behavior they qualify. Use headings that help readers find answers.
- Use consistent names for the same concepts and match commands, options, and identifiers to the implementation. Explain unfamiliar terms where the intended reader needs them.
- Follow project style for interface copy; when unspecified, use sentence case for English labels, preserving product names and identifiers.
- State the chosen behavior and relevant constraints directly. Omit references to abandoned alternatives unless their rationale helps the reader make a decision or avoid a plausible mistake.
- When correcting an unnecessary addition made during the task, describe the intended result. The correction alone does not justify a feature label, PR selling point, explanatory comment, or permanent rule.
- Ground limitations and exclusions in facts that help readers judge applicability, behavior, or consequences. Remove exclusions that merely distinguish the result from an unrelated or discarded idea.

## Verify the relevant facts

Check commands, defaults, limits, and behavior against actual sources. Distinguish source inspection, simulated verification, and live execution. Keep uncertain claims explicit and external calls within authorized scope.

Before changing text that tools interpret, verify its meaning. Preserve valid directives and necessary reasons for lint suppressions, type-check exceptions, or coverage exclusions.

For generated text, trace its source and affected outputs, then edit the source and regenerate as needed. Check summaries and reused excerpts where they appear; they must preserve the information readers need without relying on the full source text.

Follow project rules for frozen archives and third-party material. Product messages, diagnostics, and model prompts can affect behavior; handle changes to them within the authorized behavioral scope.

## Read as needed

- For calibration on completeness and brevity, read [examples](references/examples.md).
- For draft identifiers, review narration, change stories, or session-dependent references, read [session artifacts](references/session-artifacts.md).

Check final meaning, references, and applicability. Report defects and unverified claims with concrete evidence. Formatting and link checks establish structure, not semantic correctness.
