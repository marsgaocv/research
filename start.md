# Start your research project

An idea, paper, repository, or project name is enough. Use this guide yourself or with an agent.

## Choose your pace

- **Use defaults:** save the basics and what is already known. Leave unknowns as TODO. Install nothing and start no experiments.
- **Guide me:** discuss the five topics below, one at a time.

Say **skip**, **use defaults**, **later**, or **stop** whenever you like. Jump between topics, change answers, or resume another day. You do not need to answer everything.

## Five short conversations

| Topic | Discuss what matters now | Save in |
| --- | --- | --- |
| **1. Question** | What do you want to understand or improve? Narrow an idea to one question and an observable outcome. | [GOAL.md](GOAL.md), [PLAN.md](PLAN.md) |
| **2. Starting point** | Papers, code, baseline, models, and data. Check source revisions, access, licenses, sample units, splits, and possible leakage. | [PROJECT.md](PROJECT.md) |
| **3. Evaluation** | What result would change your mind? Choose a baseline and main metric. Outline inputs → train/evaluate → saved metrics: this is the project's **harness**. Reuse existing commands where possible. | PROJECT.md |
| **4. Resources** | CPU, CUDA GPU, other, or undecided? GPU count/type/VRAM and permitted devices; shared use; local/remote location and nodes; CPU/RAM, disk, time, and cost limits. Reuse compatible Python/package pins; check hardware compatibility before choosing a build. | PROJECT.md |
| **5. Skills and check** | Select relevant [skills](.agents/README.md), tracking, and an optional small check of the starting code. | PROJECT.md, [Campaign 0](campaigns/campaign0/RESULTS.md) |

PyTorch is a suggestion for new ML projects. W&B plus local TensorBoard is the tracking default; you may choose another policy. Credentials can wait until needed. Exact thresholds, sample sizes, and run budgets can wait for [campaign planning](campaigns/TEMPLATE.md), but must be fixed before the relevant experiment.

## Optional: make sure it runs

After saving the documents, offer to prepare the environment and try an existing test or small example. Skipping records **not run** and still completes setup.

1. Show environment changes, command, input, expected output, and time/cost limit. GPU work needs explicit devices and a bounded budget. Proceed within existing authorization; clarify only missing decisions.
2. Review external executable code before use. Keep a project-local environment; preserve compatible pins and check current official CPU/CUDA requirements. Do not silently upgrade shared packages.
3. Save actual commands, versions, output, failures, and spend in Campaign 0; link its RUN_LOG and root LOG.
4. Report the scope: **environment works**, **pipeline runs**, or **baseline reproduced**. An import proves only an import. Preserve failures; propose a next step without automatic retries or larger runs.

## For the guiding agent

- Read existing documents and supplied sources first. Ask one or two related questions in ordinary chat, then wait. Do not repeat answered questions or require a full literature review for setup.
- Save partial progress after useful answers. Distinguish **confirmed**, **verified** (with source), **default**, and **deferred**. Suggestions remain drafts until selected or covered by defaults; silence is not agreement.
- Keep unknown goals, data, hardware, budgets, and results unknown. CPU-only means zero GPUs; undecided means unknown. Inspecting a source does not authorize executing it or uploading data.
- Use PROJECT.md to resume. Keep scientific open questions in [BOOKKEEPING.md](BOOKKEEPING.md). Fill the original goal when agreed; preserve later changes as dated revisions. Preserve frozen protocols and evidence.
- Select optional skills explicitly, retaining pins and licenses. Do not ask for secrets in chat. Missing tracking credentials block a run requiring them, not onboarding.

## Save and finish

Summarize decisions, defaults, deferred questions, check status, and one next action in PROJECT.md. Onboarding is **basic setup saved**, **guided setup saved**, or **paused**. Experiment readiness is separate: **not assessed**, **blocked** with reasons, or **ready for a named authorized protocol**.

A project can start with every scientific detail deferred. Create its first scientific campaign when a bounded question is selected.

Conversation inspiration: [OpenRSI proposal-agent](https://github.com/OpenRSI-Foundation/OpenRSI-Index/blob/main/.agents/skills/proposal-agent/SKILL.md).
