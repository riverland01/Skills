# Skills

A collection of reusable skills created and maintained by riverland01.

| Skill | Entry point | Supporting files |
| --- | --- | --- |
| Orchestrate | [orchestrate/SKILL.md](orchestrate/SKILL.md) | UI metadata and design references in the same folder |
| Agent Swarm for Claude Code | [claude/swarm-task-orchestrator/SKILL.md](claude/swarm-task-orchestrator/SKILL.md) | Coordination records and new-skill proposal references |
| Agent Swarm for ChatGPT / Codex | [chatgpt/agent-swarm/skills/swarm-task-orchestrator/SKILL.md](chatgpt/agent-swarm/skills/swarm-task-orchestrator/SKILL.md) | Standalone skill, portable plugin, and supporting references |
| Agent Swarm conversation workflow | [chatgpt/CONVERSATION.md](chatgpt/CONVERSATION.md) | Self-contained instructions to attach or paste into a chat |

The initial upload preserves the skill files from the reviewed 19 October 2026 bundle. Orchestrate also matches the currently installed copy at upload time. The verification record below describes the checks and installation state on 19 October; this repository publication does not install any skill. Checksums cover the files in this repository, including this README.

---
# Shortened orchestration skills

Shortened 19 October 2026 after a rule-preservation review and behavioral checks. Based on the supplied `agent_swarm_skills.zip` and the user's updated orchestrate procedure.

## Choose your edition

| Edition | Location | Use |
| --- | --- | --- |
| Orchestrate | `orchestrate/` | Shortened candidate for the existing installation; portable copy with unchanged UI metadata and design reference |
| Claude Code skill | `claude/swarm-task-orchestrator/` | Copy this whole skill folder to Claude's project or personal skill location |
| ChatGPT skill and plugin | `chatgpt/agent-swarm/` | Portable instruction-only plugin; its `skills/swarm-task-orchestrator/` is also a standalone skill folder |
| ChatGPT conversation workflow | `chatgpt/CONVERSATION.md` | Attach or paste this self-contained file and explicitly ask the chat to follow it |
| Clean ChatGPT plugin ZIP | `chatgpt/agent-swarm-plugin.zip` | Contains only the plugin root for distribution through a supported plugin workflow |

The outer ZIP is a distribution bundle containing orchestrate and both swarm editions, not a universal installer. This archive does not install skills by itself. Swarm installation and publication are not performed; see the verification record for the actual orchestrate installation status.

## What changed

Both swarm editions share the same procedure and reference files:

1. Acceptance criteria map to inspected evidence, with states distinct from task completion.
2. Effort checkpoints assess progress and the next useful action while respecting explicit hard limits.
3. Dependent tasks wait for accepted prerequisite outputs; independent branches can continue.
4. Files and other mutable resources have owners; cancellation must be confirmed before handoff/finalization.
5. Changed inputs reopen affected criteria and invalidate dependent outputs while preserving unaffected results.
6. Verification separates self-checks, independent reviewers, and independent evidence/methods.
7. Decomposition, delegation, and reporting scale to the task, with no mandatory task count or universal loop caps.

### Learning now creates a different skill

The former `proposed_skill_updates` output is replaced by `proposed_new_skills`. After a verified solution, the coordinator may propose a **new problem-specific skill** for similar future problems. The proposal includes its own name and trigger, applicability, parameterized inputs and workflow, outputs and checks, demonstrated scope, and a distinct-case validation plan.

A successful decomposition remains a run record until its reusable method is extracted. Proposals and drafts do not silently change the swarm skill, install anything, or claim proven generality. Already authorized skill creation proceeds without asking for the same authorization again. Read the bundled `references/new-skill-proposals.md` for the policy and an example.

## Claude Code setup

Copy `claude/swarm-task-orchestrator/` to either `<project>/.claude/skills/swarm-task-orchestrator/` or `~/.claude/skills/swarm-task-orchestrator/`. Keep the `references/` folder beside `SKILL.md`. Invoke `/swarm-task-orchestrator <your task>`; restart the session if a newly added skill is not discovered. This edition targets Claude Code and does not assume a local install is automatically available in Cowork/cloud sessions. See [Claude skill documentation](https://code.claude.com/docs/en/skills).

## ChatGPT setup

### Desktop / native skill

The standalone folder is `chatgpt/agent-swarm/skills/swarm-task-orchestrator/`. In a local project that discovers `.agents/skills/`, copy the whole folder there, then select the skill with `@` in ChatGPT. Codex CLI/IDE users can use `$swarm-task-orchestrator`. Check skill availability in your current surface; browser chats do not automatically read local folders. See [Build skills](https://learn.chatgpt.com/docs/build-skills).

### Desktop / portable plugin

The plugin folder `chatgpt/agent-swarm/` contains root `plugin.json` and `skills/`. To use a local repository marketplace, place it at `<repo>/plugins/agent-swarm/`, then merge the entry from `chatgpt/marketplace.example.json` into `<repo>/.agents/plugins/marketplace.json`. Its relative path resolves from the repository root. Preserve existing catalog entries. Restart the desktop app, find the local marketplace in Plugins Directory, and install the plugin. Use either standalone-skill setup or plugin setup to avoid duplicate registrations. See [Package your plugin](https://developers.openai.com/plugins/build/plugins).

Native subagents depend on the current chat's capabilities. ChatGPT Work documents subagent access for eligible accounts; the skill follows actual exposed tools and otherwise works sequentially. See [Subagents](https://learn.chatgpt.com/docs/agent-configuration/subagents).

### Ordinary chat / no installer required

Attach or paste `chatgpt/CONVERSATION.md` and say:

> Use the attached Agent Swarm conversation workflow to handle the following task. Delegate useful independent work only if this chat exposes native subagent tools; otherwise execute the dependencies directly. My task is: ...

This makes the file user-invoked conversation instructions. It does not install a skill, register a command, add tools, or guarantee persistence in future chats. The file includes both supporting references, so it does not depend on a local folder.

## Verification and limitations

See `VERIFICATION.md` for the requirement mapping, actual checks and behavioral exercises, input provenance, and remaining runtime limits. File checksums are listed in `SHA256SUMS.txt`.

The download supplies instructions and supported layouts, not an execution engine or extra account permissions. Product setup facts were checked against the linked official documentation on 19 October 2026. Real Claude Code and ChatGPT account installation/execution are separate from the local package and instruction checks reported here.
