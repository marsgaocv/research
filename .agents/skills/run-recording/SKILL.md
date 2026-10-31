---
name: run-recording
description: Record or reconcile research attempts, failures, interruptions, provenance, resource spend, and permanent execution logs from actual evidence; does not launch runs.
---

# Record an attempt

Read the campaign protocol, RESULTS, RUN_LOG, relevant root [LOG](../../../LOG.md), and [recording rules](../../../AGENTS.md). Inspect the actual attempt artifacts before stating completion, spend, or success.

Identify the attempt and immutable output directory; preserve console.txt and missing-output facts. Establish UTC start/end, command/cwd, source/config/data identities, allocation, concurrency, scientific tracking, and outcome from retained evidence. Unknowns remain explicit. An absent error file is not success.

Append a root LOG entry and a campaign RUN_LOG entry that links to it and the raw evidence. Append corrections rather than rewriting history. Reconcile inclusive actual spend, original estimate, dated revisions, difference/ratio, and cumulative totals; avoid double-counting overlapping ledgers. Update RESULTS in place and root CAMPAIGN's spend/status. Scientific verdict changes need evidence against the frozen criteria.

For an interrupted run, record last known state, partial outputs, unknown end/spend, and permitted next action. Do not restart, signal processes, query GPUs, sync external data, or launch monitoring as part of log reconciliation.

Return the evidence links, reconciled accounting, unresolved unknowns, and next action. Separate execution completion from scientific interpretation.
