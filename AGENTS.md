# Research agent rules

Start with README, PROJECT, GOAL, PLAN, CAMPAIGN, BOOKKEEPING, and FINDINGS; consult relevant logs and evidence. New projects begin at [start.md](start.md). Report negative results honestly.

## Scope

- User instructions govern the task. GOAL holds direction, PROJECT holds settings, and campaign protocols hold frozen designs and budgets.
- Setup may finish with TODOs. Never invent data, hardware, budgets, permission, results, or novelty to fill a gap.
- Proceed when the task, budget, and correctness gates authorize work; avoid repeated confirmation. Roadmaps, skills, and available devices do not authorize extra experiments, sweeps, retries, or scope changes.
- Preserve original goals, configurations, raw evidence, and verdicts. Amend explicitly; never change criteria to fit observed results.

## Research

- One goal, hypothesis, and claim per campaign. State **RESOLVES** or **EVIDENCE TOWARD**; separate independent questions.
- Check primary prior work. Label established methods, incremental changes with their parents, and provisional novelty. An unsuccessful search does not prove novelty.
- Freeze endpoints, practical thresholds, splits, independent units, seeds/replication, aggregation, uncertainty, controls, and stopping before held-out evaluation. Pilots are scale-limited; nonsignificance is not equivalence.
- Check provenance, licenses/access, leakage, and domain correctness. Pin code/data/model/tokenizer revisions as applicable; audit remote code before execution.
- Validate method-defining behavior against a reference before optimization. Declare precision/backend changes and parity gates; framework advice cannot redefine the method.
- Match useful work and count overhead/failures. Separate training, inference, adaptation, preprocessing, and evaluation claims. Qualify shared-device timing unless contention is controlled.
- Review evidence before spending. Choose adequate scale; justify larger runs when needed. Do not scale to conceal correctness failures or chase positives.

## Resources and tracking

- Follow [the budget-first contract](campaigns/TEMPLATE.md): allocation, measured basis, uncertainty, inclusive cost, cap, stop rule, and decision bought. Compare scientific value and cheaper equally decisive alternatives. Revise budgets before overruns; unknown spend is TODO, not zero.
- Use explicit permitted devices. Take one host-shell device snapshot for an authorized GPU launch and reuse it. Failed queries mean UNKNOWN. No polling, driver resets, continuous GPU/system collectors, or standalone CUDA probes.
- Shared use is allowed when memory fits and contention is budgeted. Preserve existing jobs. Never signal a process you did not start; ownership alone does not authorize stopping unrelated work.
- Default: W&B plus local TensorBoard. A project may select another policy before running. Missing required credentials block experiments, not setup; retain local logs during outages. Keep secrets outside repository files.
- Log run/config/code/data identities, scientific metrics, application-reported memory/throughput, and resource time. Disable automatic system/metadata/machine collection. External data uploads need authorization.

## Code and records

- Reusable code: src/. Commands: scripts/. Shared configs: configs/. Local datasets: data/. Campaigns hold protocols and artifacts; any run.sh is a thin launcher.
- Keep pinned vendor sources unchanged; put adapters in src/. Choose runtime, precision, and hardware per project.
- Every campaign keeps fixed RESULTS.md and RUN_LOG.md. Update RESULTS; append RUN_LOG. Separate execution status from scientific verdict. Link RESULTS from root README and CAMPAIGN.
- Attempts use campaigns/campaignN/results/<run_id>/console.txt. Reports/figures go in reports/; design/audits in docs/. External bulky artifacts need campaign-local hash/retrieval manifests.
- Append root LOG records: UTC start/end, run/rung, command/cwd, source/config/data identities, allocation/concurrency, tracking, estimate/actual/variance, outcome, evidence, cumulative spend, next action. Include failures; unknown crash end/spend stays unknown until recovered.
- Campaign 0 records infrastructure; use N/A where tracking/devices do not apply. CPU-only checks cost zero GPU-hours. CPU-only scientific experiments still need a scientific campaign and budget.

## Storage

- Retain one latest resumable checkpoint and one best development checkpoint per arm/seed. Freeze selection metric/direction/cadence; keep earlier best on ties and reject nonfinite scores. Never select on test outcomes.
- Latest includes optimizer/scheduler, RNG, data cursor, and identities for continuation. Best-only weights need selection metadata. Share identical latest/best weights; extra snapshots require a named purpose.
- Publish rolling saves atomically with integrity manifests before pruning. Budget in-flight disk, RAM, and VRAM separately; stream data/hashing and bound caches/workers.
- Before authorized cleanup, check writers/dependencies and record paths, sizes, hashes, reasons, retained references, and verified backup status. Keep scores, logs, protocols, provenance, and deletion history. Retraining is not a backup.

## Skills and writing

Use relevant [skills](.agents/README.md), loading only needed references. Review optional instructions/scripts; retain pins and licenses. Skills grant no extra authorization. Read PLOTTING before figures.

| File | Rule / ceiling |
| --- | --- |
| README | Orientation/pointers; three-sentence introduction; ≤150 lines |
| GOAL | Preserve original; date revisions with evidence or user direction; ≤60 lines |
| CAMPAIGN | Idea, conclusion, spend; ≤6 lines/campaign, ≤120 total |
| BOOKKEEPING | Current understanding; Git preserves revisions; ≤100 lines |
| FINDINGS | Qualifying evidence; ≤80 lines; otherwise exactly “No qualifying findings yet.” |
| LOG / campaign RUN_LOG | Append-only; append corrections; no ceiling |

Keep root summaries concise; link campaign detail instead of recounting attempts. Preserve original goal history before moving overflow. Keep setup skippable and respect existing choices.
