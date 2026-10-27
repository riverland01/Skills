# Skills

Reusable skills created and maintained by riverland01, organized by **skill → target system**.

| Skill | Purpose | Available editions |
| --- | --- | --- |
| [Orchestrate](orchestrate/README.md) | Coordinate complex work through selective delegation, synthesis, and verification | [Codex](orchestrate/codex/SKILL.md) |
| [Agent Swarm](agent-swarm/README.md) | Coordinate tasks and propose separate skills from verified reusable methods | [Claude](agent-swarm/claude/SKILL.md), [ChatGPT](agent-swarm/chatgpt/agent-swarm/skills/swarm-task-orchestrator/SKILL.md) |
| [Grill Me](grill-me/README.md) | Clarify and challenge complex plans and decisions through adaptive questioning | [Codex](grill-me/codex/SKILL.md), [Claude](grill-me/claude/SKILL.md) |

```text
orchestrate/
  README.md
  codex/                 # Skill, UI metadata, and references
agent-swarm/
  README.md
  claude/                # Skill and references
  chatgpt/               # Skill/plugin package and conversation workflow
grill-me/
  README.md
  codex/                 # Skill, UI metadata, and references
  claude/                # Skill and references
  releases/              # Complete skill ZIPs
  verification/          # Review records and synthetic evidence
docs/                    # Shared verification record and checksums
```

Each skill's README explains its editions and package locations. Future editions belong under their skill's folder, using the target system's name.

The [verification record](docs/verification-2026-10-19.md) documents the original review and its limits. [SHA-256 checksums](docs/SHA256SUMS.txt) cover the current files; paths are relative to the repository root.
