# Session Artifacts and Overcorrection

Could a reader without the authoring conversation understand the facts, resolve references, and check the evidence? Judge meaning rather than deleting by keyword.

| Suspect passage | Treatment |
| --- | --- |
| “Per review C2” or “design discussion item 7” | Cite an accessible named record, or state the necessary fact independently |
| “This PR adds” in current-state guidance | State the effective mechanism |
| “The reviewer confirmed this is safe” | State the safety condition; delete if no unique proposition remains |
| A comment that merely repeats a loop, branch, or assertion without explanatory value | Keep non-obvious constraints or verification rationale; preserve steps and reasoning that serve a teaching purpose in tutorials or algorithm explanations |
| “Probably sufficient for now” | Name the known bound and uncertainty |
| “Uses A, without B” where B is an abandoned, irrelevant idea | State A; retain B only if the exclusion matters to the reader's task |

Preserve:

- Runtime ordering: “The old connection drains before the new one accepts requests.”
- Regression conditions: “Without deduplication, the same task may run twice.”
- Measurement sources, versions, scale, and conditions.
- Valid issue, standards, and historical-evidence references relevant to the document's purpose.
- Genuine uncertainty in proposals and causal sequence in incident records.

A coverage exclusion explaining that a branch requires an unavailable platform may carry both executable directive syntax and a maintenance constraint. Check the reason against the code and test environment; preserve a valid directive and its necessary rationale. A false reason calls for an evidence-based correction of the exclusion or explanation, not automatic deletion as review narration.

Before trimming, check that obligations remain obligations, proposals remain proposals, and evidence keeps its source.
