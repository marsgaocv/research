# Create a campaign

Select one bounded question tied to [GOAL](../GOAL.md). Read [standing rules](../AGENTS.md), current evidence, and the budget contract below. Creating documents does not authorize execution.

1. Choose the next unused positive integer N. Never reuse or overwrite an existing campaign directory; Campaign 0 is infrastructure.
2. Create campaigns/campaignN/ with docs/, results/, and reports/. Copy the [protocol](templates/campaign.md), [results](templates/RESULTS.md), and [run log](templates/RUN_LOG.md) into it; rename campaign.md to campaignN.md. Replace N and the protocol link token. Template-relative root links already have the correct depth after copying.
3. Fill the protocol progressively. TODOs are allowed during planning; resolve requirements for the proposed run before launch.
4. Add the campaign's RESULTS link to root CAMPAIGN and README, with status **planning**, verdict **not evaluated**, and no implied allocation. Append creation/authorization records only for events that actually occurred.
5. Record each attempt under a new results/<run_id>/ with console.txt; update RESULTS, append RUN_LOG/root LOG, and reconcile cumulative spend after every attempt or recovery.

## Budget first

Record expected cost separately from contingency and hard cap. GPU-hours = sum(devices × wall hours × repetitions) across arms. Include controls, feasibility, evaluation, compilation, saves, failed/aborted work, and authorized retries. CPU/API-only work uses appropriate time/currency units and zero GPU allocation.

State allocation/concurrency, closest measured workload and its limitations, RAM/VRAM/disk requirements, in-flight storage, uncertainty, and stop conditions. Compare scales by scientific decision value and opportunity cost. Use the cheapest equally decisive alternative; justify sufficient exposure, precision, or replication rather than habitual tiny pilots. Unknown critical resource inputs mean not ready to run.

Preserve original estimates; date revisions before spending more. Record actual−estimate and actual/estimate (undefined for zero estimate), measurement method, uncertainty, and campaign totals including failures.

## Scientific contract

Exactly one goal, hypothesis, and claim. Define win, not-win, and inconclusive outcomes with practical thresholds and uncertainty. Freeze endpoints, data provenance/splits, leakage checks, independent units, replication/seeds, controls/falsifier, analysis, stopping, and config before held-out outcomes. State what is RESOLVED versus EVIDENCE TOWARD and the confirmation scale. Negative evidence is a useful decision; an underpowered null is not equivalence.

For efficiency comparisons, match useful work/data/targets/updates and evaluation workloads, or freeze resource ceilings for capacity comparisons. Predefine quality and minimum cost/capacity thresholds. Count all method overhead; separate training, prefill/inference, and adaptation. Nominal compression or memory fit is not measured quality-qualified efficiency. Shared-device timings remain descriptive without valid contention control.

## Findings

Promote evidence only when it supports publication or materially changes the plan with adequate controls and replication for the claim. Record exact claim, output/provenance links, strength, tested scale, independent replications, RESOLVES/EVIDENCE TOWARD, scale limitations, confirmation needed, and surviving alternatives. Supported negatives may qualify; isolated failures and weak nulls do not.

## Closeout

Keep RESULTS.md and RUN_LOG.md filenames fixed. Separate execution state from verdict. Report what happened, uncertainty, surviving explanations, budget variance, retention/backup status, and **What might we be missing?** Update root synthesis without copying operational history. Closure does not authorize rerunning or scaling.
