# Research skills

Standing rules live in [AGENTS.md](../AGENTS.md). Skills are reusable procedures in `.agents/skills/<name>/SKILL.md`; they are committed with this template. Read only the skill relevant to the current task.

| Included skill | Use it for |
| --- | --- |
| [research-setup](skills/research-setup/SKILL.md) | Defaults or guided setup, resumption, optional first check |
| [campaign-planning](skills/campaign-planning/SKILL.md) | One budgeted question and its experiment protocol |
| [run-recording](skills/run-recording/SKILL.md) | Actual attempts, interruptions, resource accounting, and logs |
| [research-synthesis](skills/research-synthesis/SKILL.md) | Evidence, limits, current understanding, and next decisions |

In Codex, ask “Use $research-setup to help me start,” or simply ask the agent to read [start.md](../start.md). Tools without skill discovery can read the linked files directly. See [official skill documentation](https://learn.chatgpt.com/docs/build-skills) for discovery behavior.

These four instruction-only skills are original template content under the root MIT license. They install no frameworks and do not authorize compute or external actions. The same rules apply when a skill is selected automatically.

## Optional specialists

See the [pinned catalog](catalog.md) for six optional starting references. None is installed by this template. Select only skills relevant to the project; inspect the pinned instructions, examples, dependencies, and upstream license before installation. Record installed sources, immutable revisions, file hashes, local modifications, and licenses in this directory and PROJECT.md. Keep the skill files and required license notices in Git.

An optional skill's package, monitoring, sweep, or GPU examples do not override project rules. Installation is separate from permission to run its scripts, change dependencies, download models, or upload data. Review proposed updates explicitly and retain prior provenance in the project log.
