# research

A Markdown-first starting point for machine learning and AI-for-science projects.
Keep research goals, experiment decisions, evidence, and compute costs together as the project evolves.
Start with the basics or let an agent guide you through a short, skippable setup.

## Start here

1. Select **Use this template → Create a new repository** on GitHub, then clone your new repository. Alternatively, copy these files into a new directory and initialize independent Git history.
2. Open [start.md](start.md), or ask your coding agent:

   > Read start.md and help me set up this research project.

3. Choose **Use defaults** or **Guide me**. You can skip any question, stop, resume, or change your mind.

No packages are required to use this template. It contains documents and skills, with empty working directories; packages and research code are selected for each project during setup. Setup can finish while the goal, data, or compute details remain undecided. Running an experiment needs its own concrete protocol and budget.

## Research workflow

Establish a goal → investigate prior work and starting code → plan one campaign → validate the setup → run the authorized comparison → record every attempt → update the evidence and next decision.

Use [the campaign guide](campaigns/TEMPLATE.md) to create a campaign manually or with an agent. A campaign has one hypothesis, a budget, and a decision it can change. Failed runs and negative results remain part of the record.

## Documents

| Document | Purpose |
| --- | --- |
| [start.md](start.md) | Defaults or guided onboarding, including an optional first check |
| [PROJECT.md](PROJECT.md) | Environment, resources, harness, skills, and setup progress |
| [GOAL.md](GOAL.md) | Original research goal and dated changes |
| [PLAN.md](PLAN.md) | Current roadmap and next bounded decision |
| [AGENTS.md](AGENTS.md) | Standing research and implementation rules |
| [CAMPAIGN.md](CAMPAIGN.md) | Campaign index, verdicts, and spend |
| [BOOKKEEPING.md](BOOKKEEPING.md) | Current understanding and open questions |
| [FINDINGS.md](FINDINGS.md) | Evidence strong enough to change the plan or support publication |
| [LOG.md](LOG.md) | Permanent execution and infrastructure records |
| [PLOTTING.md](PLOTTING.md) | Scientific figure and provenance conventions |
| [.agents/README.md](.agents/README.md) | Included workflow skills and optional specialist catalog |

## Working directories

| Path | Contents |
| --- | --- |
| `src/` | Reusable research implementation, created when needed |
| `scripts/` | Project-specific commands and thin launchers, created when needed |
| `tests/` | Correctness checks for the selected implementation |
| `configs/` | Shared configurations; freeze actual run configs with each attempt |
| `data/` | Local datasets, ignored by Git; provenance belongs with campaigns |
| `vendor/` | Optional pinned upstream sources; use local adapters for changes |
| `campaigns/campaignN/` | Protocol, results, run index, and all campaign artifacts |

## Campaign entry points

| Campaign | Current result | Execution history |
| --- | --- | --- |
| 0 — infrastructure | [RESULTS.md](campaigns/campaign0/RESULTS.md) | [RUN_LOG.md](campaigns/campaign0/RUN_LOG.md) |

W&B plus local TensorBoard is the default experiment-tracking policy; another policy can be explicitly selected during setup. Credentials, raw data, weights, and local tracking payloads stay out of Git. Review the actual staged files before publishing; ignore rules cannot detect every sensitive file.

Template content is [MIT licensed](LICENSE). Optional tools, datasets, models, and upstream code retain their own licenses.
