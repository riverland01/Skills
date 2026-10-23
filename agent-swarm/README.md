# Agent Swarm

Coordinate tasks with acceptance criteria, dependency handoffs, ownership, effort checkpoints, and verification. Checked reusable methods may support proposals for separate problem-specific skills.

## Claude

The complete skill is in [claude/](claude/), with [SKILL.md](claude/SKILL.md) and its `references/` folder. When installing it, copy the complete folder into the supported skill location with the destination folder named `swarm-task-orchestrator`.

## ChatGPT

| Format | Location | Use |
| --- | --- | --- |
| Standalone skill | [swarm-task-orchestrator/](chatgpt/agent-swarm/skills/swarm-task-orchestrator/) | Copy the complete skill folder into a supported skill location |
| Portable plugin | [agent-swarm/](chatgpt/agent-swarm/) | Complete package containing `plugin.json` and `skills/` |
| Plugin ZIP | [agent-swarm-plugin.zip](chatgpt/agent-swarm-plugin.zip) | Archive of the same plugin package |
| Conversation workflow | [CONVERSATION.md](chatgpt/CONVERSATION.md) | Attach or paste into a chat and explicitly request its use |
| Marketplace example | [marketplace.example.json](chatgpt/marketplace.example.json) | Example entry pointing to the plugin's location in this repository |

The standalone skill's runtime adapter also supports Codex; it uses the same package. The marketplace example's source path resolves from the repository root. Preserve existing entries when incorporating it into a supported local marketplace.

For the conversation format, supply the file with your task and ask the chat to follow the workflow. It includes its supporting references. Actual delegation depends on the tools available in the current environment.

Skill instructions, references, plugin contents, and the conversation workflow retain the reviewed 19 October 2026 contents. See the shared [verification record](../docs/verification-2026-10-19.md) for review coverage and runtime limits.
