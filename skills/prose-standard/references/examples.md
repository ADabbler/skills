# Editorial Calibration

## Preserve timing and failures

Original: “The exporter carefully writes to a temporary file, replaces the destination only after the write succeeds, and reports failures to the caller.”

Balanced: “The exporter writes to a temporary file, replaces the destination only after the write succeeds, and reports failures to the caller.”

Over-trimmed: “The exporter saves the file.” This loses the intermediate destination, replacement condition, and failure reporting.

## Explain the consequence of configuration order

Redundant: “Load the policy plugin, then the tools plugin,” when the configuration already lists that order.

Useful: “Load policy before tools so tool writes pass through permission checks.”

## Keep necessary local behavior

Insufficient: “See the cancellation design note.”

Balanced: “Cancellation aborts the request and waits for workers to exit. See the design note for ownership and race handling.”

## Describe useful limitations

Useful: “The application reads configuration at startup; configuration changes require restart.”

Irrelevant to user guidance: “Private helpers should eventually use consistent names.”

## State the adopted design

Distracting: “The application reads configuration at startup, without the abandoned file-watching mechanism.”

Useful: “The application reads configuration at startup.”

Explain an alternative when the comparison helps the reader understand a tradeoff or avoid misuse.

Useful exclusion: “Preview shows the planned changes without writing files.” Readers rely on this guarantee when deciding whether to run the command.

## Correct unnecessary additions without manufacturing a requirement

Task: add CSV export. The agent also adds an unrequested dashboard, then removes it when corrected.

Final description: “Add CSV export.”

“CSV export without a dashboard” and a comment explaining why dashboards are excluded preserve the agent's detour rather than useful product knowledge. A durable restriction requires independent requirements or evidence.

## Preserve verification scope

Unsupported: “Works on all platforms,” after testing only on Linux.

Accurate: “The Linux installation flow is verified; Windows and macOS remain unverified.”

## Ground rationale in evidence

If code establishes only a 30-second timeout, record that fact. “Balancing performance and reliability” requires evidence before being attributed as the historical reason.
