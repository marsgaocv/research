# Research agent rules

Read README, PROJECT, GOAL, PLAN, CAMPAIGN, BOOKKEEPING, and FINDINGS for orientation; consult LOG and campaign evidence for relevant attempts. For a new project, follow [start.md](start.md). This is research: report negative results and do not optimize the story for success.

## Authority and scope

- User instructions govern the task. GOAL holds research direction, PROJECT holds local settings, this file holds standing rules, and campaign protocols hold frozen designs and allocations. Historical notes do not authorize new work.
- Setup can finish with deferred decisions. Do not confuse completed onboarding with experimental readiness. Do not invent missing data, hardware, budgets, approvals, results, or novelty.
- Execute work already covered by the task, budget, and correctness gates without repeated confirmation. A roadmap, installed skill, or available device does not authorize an experiment, sweep, retry, or scope change.
- Preserve original goals, configurations, raw evidence, and verdict history. Amend explicitly; do not retrofit criteria after seeing results.

## Scientific design

- Each campaign has one goal, one hypothesis, and one claim tied to the current project goal; separate independent questions. Distinguish RESOLVES from EVIDENCE TOWARD.
- Check primary prior work before proposing a method or claiming novelty. Label established work, incremental variations with their parents, and provisional novelty. A failed search is not evidence of novelty.
- Freeze endpoints, practical effect thresholds, data splits, independent units, seeds/replication, aggregation, uncertainty, stopping, and controls before held-out evaluation. Pilot evidence remains scale-limited; nonsignificance does not establish equivalence.
- Check data provenance, licenses/access, contamination, and domain-specific correctness. Pin model, data, tokenizer, and code revisions when relevant. Audit remote executable code before use.
- Validate method-defining behavior against an appropriate reference before optimizing it. Framework advice does not override the intended scientific method. Declare precision/backend changes and required parity gates.
- Compare matched useful work. Separate training, inference, adaptation, preprocessing, and evaluation claims; count overhead and failed attempts. Shared-device timing is descriptive unless contention is controlled and documented.
- Review existing evidence before spending. Choose the smallest adequately discriminating scale; justify larger allocations when smaller ones cannot answer the question. Do not scale to hide correctness failures or chase a positive result.

## Compute and tracking

- Use [the budget-first contract](campaigns/TEMPLATE.md). State devices × wall hours × repetitions across all arms, CPU/API costs when relevant, controls, evaluation, failure allowance, measured basis, uncertainty, hard cap, and scientific decision bought. Parallelism changes elapsed time, not total device-hours.
- Compare candidate scales and the cheapest equally decisive alternative. Prioritize scientific value per resource unit, including informative negatives. Revise allocations before overruns; unknown spend is TODO, never zero.
- Select explicit devices from PROJECT's permitted resources. On a relevant authorized GPU launch, take one ordinary host-shell device snapshot and reuse it. Query failure means UNKNOWN; no polling, driver reset, continuous GPU/system collectors, or standalone CUDA probes.
- Shared occupancy is not itself a veto: check memory fit, preserve existing jobs, and account for contention. Never signal a process you did not start; ownership alone does not authorize stopping unrelated work.
- Default tracking is W&B plus local TensorBoard; a project may explicitly select another policy before execution. Missing required credentials block experiments, not document setup. Preserve local logs during service outages; never embed secrets in repository files.
- Log campaign/run identity, resolved config, Git SHA and dirty-state evidence, revisions, scientific metrics, application-reported memory/throughput, and allocated resource time. Disable automatic system/metadata/machine collection. No unapproved external data uploads.

## Implementation and artifacts

- Reusable code belongs in src/, commands in scripts/, shared configs in configs/, and shared local datasets in data/. Campaigns hold protocols and artifacts, not reusable implementation. A campaign run.sh, if added, is a thin launcher.
- Keep pinned vendor sources unchanged; put adapters in local source. Choose framework, precision, runtime, and hardware requirements per project rather than inheriting this template author's machine.
- Every campaign has fixed RESULTS.md and RUN_LOG.md from creation. Update RESULTS in place; append attempts, stops, resumes, and recovery to RUN_LOG. Keep execution status separate from scientific verdict. Root README and CAMPAIGN link to RESULTS.
- Keep immutable attempts in campaigns/campaignN/results/<run_id>/ with console.txt. Reports/figures go in reports/, supporting design/audits in docs/. No campaign artifacts in root report directories. Large external storage needs a campaign-local hash/retrieval manifest.
- Append root LOG records with UTC start/end, run/rung, exact command/cwd, code/config/data identities, devices/concurrency, tracking paths, estimate/actual/variance, result, and evidence links. Include failures. Crashes may leave end time and spend unknown until recovery.
- Infrastructure records use Campaign 0, with tracking/devices N/A when inapplicable and zero GPU-hours only for known CPU-only checks. CPU-only scientific experiments still require a scientific campaign and a budget.

## Retention

- Default per arm/seed: one latest resumable checkpoint plus one best development checkpoint. Freeze selection metric/direction/cadence; keep earlier best on ties and reject nonfinite scores. Never select on test outcomes.
- Latest includes optimizer/scheduler, RNG, data cursor, and identities for continuation. Best-only weights need selection metadata, not duplicated optimizer state. Share identical latest/best weights; keep extra final/reference weights only for a named dependency.
- Publish rolling saves atomically with integrity manifests before pruning predecessors. Budget in-flight disk, RAM, and VRAM separately. Stream data/hashing and bound caches/workers.
- Before authorized cleanup, check writers and dependencies; record paths, sizes, hashes, reason, retained references, and verified backup status. Preserve scores, logs, protocols, provenance, and deletion history. Rerunning training is not a backup.

## Skills and documentation

Use the relevant [workflow skill](.agents/README.md); load only applicable references. Skills guide procedure, not scientific authorization. Review optional skills and their executable examples before use; preserve source pins and licenses.

| File | Maintenance rule / ceiling |
| --- | --- |
| README | Orientation and pointers; three-sentence introduction; ≤150 lines |
| GOAL | Original goal preserved; dated changes with evidence or “user direction; no finding”; ≤60 lines |
| CAMPAIGN | Idea, conclusion, current spend; ≤6 lines per campaign and ≤120 total |
| BOOKKEEPING | Rewrite current understanding; Git retains prior versions; ≤100 lines |
| FINDINGS | Qualifying evidence only; ≤80 lines; otherwise exactly “No qualifying findings yet.” |
| LOG / campaign RUN_LOG | Append-only; corrections appended; no length ceiling |

Move overflow into campaign records with links; preserve originals before shortening frozen goal history. Keep root summaries free of run-by-run narration. Read PLOTTING before figures. Skills and setup instructions should stay brief, skippable, and consistent with the user's current choices.
