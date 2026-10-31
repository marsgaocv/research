# Start your research project

You do not need a complete proposal to start. An idea, a paper, a repository, or just a project name is enough. This guide works with an agent or as a manual checklist.

## Choose your pace

**Use defaults:** keep the basic workflow and fill only what is already known. No interview is required. Unknown goals, data, hardware, and budgets stay TODO; no packages are installed and no experiments are started.

**Guide me:** discuss the five topics below, one at a time. Answer only what is useful now. Say **skip**, **use defaults**, **come back later**, or **stop** at any point. You can also jump to a topic or ask the agent to suggest options.

For an agent, begin with: “Would you like the basics with defaults, or a short guided setup? Either way, you can skip anything.” If the user already chose a mode, honor it without asking again.

## How the conversation works

- Read existing project documents and supplied repositories before asking for facts available there. Preserve existing work and explicit choices.
- Ask one or two short, related questions per turn in ordinary chat, then wait for the reply. Avoid a long questionnaire. Give a brief explanation or a few options when that makes answering easier.
- Accept partial answers. Record what is known, summarize the current choice, and move on when the user skips. Silence is not consent.
- Update the relevant documents after each useful answer. Use the labels **confirmed**, **verified** (with source), **default**, and **deferred** where the distinction matters. Do not duplicate the same settings in several files.
- Resume from PROJECT.md: recap the saved state briefly and ask only what remains relevant. A changed answer updates the plan; preserve frozen goals, protocols, and run evidence through dated amendments.
- Recommendations are drafts until selected or covered by “use defaults.” Do not manufacture scientific decisions to make documents look finished.

## 1. Research direction

Start with: “What would you like to understand or improve?” Help narrow a broad idea to one question, one proposed change, and an observable outcome. An initial hypothesis can be provisional; a numerical success threshold can wait for campaign planning.

Save the agreed original goal in [GOAL.md](GOAL.md), candidate directions and the next decision in [PLAN.md](PLAN.md), and unresolved scientific questions in [BOOKKEEPING.md](BOOKKEEPING.md). If the user has no goal yet, retain a specific TODO rather than inventing one. Fill the original-goal placeholder once it is agreed; subsequent goal changes are dated additions.

## 2. Starting materials

Ask whether there is a paper, local folder, GitHub repository, model/checkpoint, or dataset to start from. Existing code is optional. Inspect supplied sources; record an immutable revision when available, relevant entry points, access requirements, licenses, and what has actually been reproduced.

Discuss data availability, approximate size, units of observation, proposed splits, and likely leakage only as relevant. Restricted or unavailable data can remain deferred. Do not upload data or execute downloaded code just to inspect it. A short primary-source literature check can clarify the baseline; this is not a demand for a full literature review.

Save sources and data settings in [PROJECT.md](PROJECT.md). Record uncertain assumptions in BOOKKEEPING. Novelty remains unverified until the appropriate literature check is done.

## 3. Evaluation and a small harness

Ask: “What result would help you decide whether the idea is worth pursuing?” Identify a plausible baseline, main metric and direction, evaluation units, and a fair comparison. Defer exact thresholds or sample sizes until there is a basis for them; freeze them before held-out results.

Here, a **harness** means the project's ordinary input → train or evaluate → metrics and artifacts workflow. Reuse an existing harness if it works. Record input/output locations, commands, metric aggregation, tracking, and expected outputs in PROJECT.md. No particular orchestration framework is required. If code does not exist yet, record the smallest next implementation task rather than claiming the pipeline runs.

## 4. Compute, Python, and packages

Discuss CPU, CUDA GPU, another accelerator, or “decide later.” For GPU work, capture available count, model, VRAM, which devices may be used, and whether they are shared. Capture local/remote location, node count, CPU/RAM, disk capacity, and time/cost limits when relevant. Availability and permission are different facts; neither should be guessed.

Inspect existing dependency files and compatible environments first. Reuse project pins where possible. For a new ML project, PyTorch is a suggestion, not an installed default. Select a CPU/CUDA build only after checking intended hardware and current official compatibility guidance. Keep a project-local environment; do not silently upgrade a shared one. Record Python, package manager, package pins, install commands, and runtime requirements in PROJECT.md.

Resource estimates may remain unknown during onboarding. A later run needs a numeric budget covering all arms, checks, evaluation, and failures. CPU-only means zero GPUs; undecided hardware means unknown, not zero available GPUs.

## 5. Skills, tracking, and an optional first check

The four [workflow skills](.agents/README.md) are already included. Suggest specialist skills only for the chosen work; show their source and scope before installation. Preserve pinned provenance and licenses. Skill installation does not install its example dependencies or authorize runs.

Default tracking is W&B plus local TensorBoard. Configure project/entity and credential locations only when needed; never ask the user to paste secrets into chat or documents. Missing credentials do not block documentation setup. They block a run requiring that tracker unless the user explicitly chooses another policy first.

After saving the setup, offer: “Would you like to prepare the environment and try a small check of the starting code, or leave that for later?” If skipped, record **not run**. If selected:

1. Show the proposed environment changes, exact command, input, expected output, allocation, and maximum duration/cost. Confirm only decisions not already covered by the user's authorization.
2. Reuse a relevant existing test or small end-to-end example. Review external executable code first. GPU work needs explicit devices and a bounded allocation; do not run a standalone GPU probe or begin training as an implicit setup action.
3. Save commands, revisions, console output, observed results, and spend under [Campaign 0](campaigns/campaign0/RESULTS.md), with an entry in its RUN_LOG and root LOG. Record an absent output as missing.
4. Report exactly what passed: **environment works**, **pipeline runs**, or **baseline reproduced**, with the tested scope. An import is not a baseline reproduction. On failure, preserve the evidence and suggest the next action; no automatic retry or larger run.

## Finish now, return later

Write a short setup summary in PROJECT.md: decisions made, defaults used, deferred questions, check status, and the next useful action. Set onboarding to **basic setup saved**, **guided setup saved**, or **paused**. Track experiment readiness separately: **not assessed**, **blocked** (with concrete missing requirements), or **ready for a named authorized protocol**.

A user can finish setup with all scientific details deferred. Defaults establish the workflow, not a research claim or compute permission. Do not create a scientific campaign until a bounded question is selected. When ready, use [campaigns/TEMPLATE.md](campaigns/TEMPLATE.md).

Interaction inspiration: [OpenRSI proposal-agent](https://github.com/OpenRSI-Foundation/OpenRSI-Index/blob/main/.agents/skills/proposal-agent/SKILL.md). This guide uses a lightweight, skippable conversation and does not adopt that system's proposal eligibility or execution architecture.
