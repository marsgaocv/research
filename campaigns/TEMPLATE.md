# Create a campaign

A campaign answers one question tied to [GOAL](../GOAL.md). Read [AGENTS](../AGENTS.md) and relevant evidence first. A planning document is not permission to run.

## Create the folder

1. Choose the next unused positive number N; Campaign 0 is infrastructure. Never overwrite a campaign.
2. Create campaigns/campaignN/ with docs/, results/, and reports/. Copy the [protocol](templates/campaign.md), [results](templates/RESULTS.md), and [run log](templates/RUN_LOG.md). Rename campaign.md to campaignN.md; replace N and add the protocol link in RESULTS. Relative links work at this depth.
3. Add the RESULTS link to root CAMPAIGN and README: **planning**, **not evaluated**, no allocation implied.
4. Fill the protocol. TODOs are fine while planning; resolve run requirements before launch.

## Budget before design

**GPU-hours = sum(devices × wall hours × repetitions)** across all arms. Include checks, controls, evaluation, compilation, saves, failures, and authorized retries. Use CPU time/API costs where applicable. Parallelism does not reduce total device-hours.

Record the measured basis, uncertainty, allocation, RAM/VRAM/disk, in-flight saves, expected cost, contingency, hard cap, and stopping rule. Explain the decision bought, plausible positive/negative outcomes, and why a cheaper comparison would be less decisive. Critical unknowns block execution.

Preserve estimates and date revisions before extra spending. Record actual−estimate and actual/estimate (undefined for zero), timing uncertainty, and inclusive totals.

## Freeze the question

- One goal, hypothesis, and claim; practical win/not-win/inconclusive criteria.
- Endpoints, splits/provenance, leakage checks, independent units, seeds/replication, uncertainty, controls/falsifier, analysis, stopping, and configuration before held-out results.
- **RESOLVES** or **EVIDENCE TOWARD**, tested scale, limitations, and needed confirmation. A weak null does not establish equivalence.
- For efficiency: match useful work or freeze capacity-test resources; set quality and minimum cost/capacity thresholds. Count overhead and separate training, inference, and adaptation. Memory fit is not quality-qualified efficiency; shared-device timing needs qualification.

## Record and decide

Each attempt gets results/<run_id>/console.txt. Update RESULTS in place; append RUN_LOG and root LOG with evidence links and inclusive spend. Keep those filenames fixed through failures, stops, recovery, and closure.

Separate execution status from scientific verdict. Explain uncertainty, remaining alternatives, budget variance, retention/backup status, next action, and **What might we be missing?** Closure does not authorize another run.

Promote findings only with adequate controls and replication for the claim. Record claim, evidence/provenance, strength, tested scale, independent replications, RESOLVES/EVIDENCE TOWARD, limitations, and confirmation needed. Supported negatives can qualify; isolated failures and weak nulls cannot.
