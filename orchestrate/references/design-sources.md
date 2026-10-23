# Design sources

These references informed the design agreed in the build brief. They are optional maintenance resources, not runtime dependencies. Inspect current upstream instructions before adapting further material; preserve this skill's selective, cross-domain scope.

| Source | Adopted pattern |
| --- | --- |
| [OpenAI Codex orchestrator template](https://github.com/openai/codex/blob/main/codex-rs/core/templates/agents/orchestrator.md) | Root coordination, independent parallel work, waiting, avoiding duplication. |
| [OpenAI code-review routing](https://github.com/openai/codex/blob/main/.codex/skills/code-review/SKILL.md) | Fan out across relevant dimensions and aggregate findings. |
| [OpenAI research routing](https://github.com/openai/plugins/blob/main/plugins/life-science-research/skills/research-router-skill/SKILL.md) | Normalize scope, delegate evidence gathering, retain conflict resolution and synthesis at the root. |
| [Gentle-AI](https://github.com/Gentleman-Programming/gentle-ai) | Dependency-aware handoffs, collection and artifact checks, capability-aware fallback. Software-specific phases are not mandatory here. |
| [provencher/codex-skills — orchestrate](https://github.com/provencher/codex-skills) | Compact contracts, distinct ownership, leaf workers, parent integration. |
| [Superpowers](https://github.com/obra/superpowers) | Focused contexts and independent review. Fixed software-development ceremonies are not adopted. |

Installation is separate from execution. Use the current environment's supported user-level skill location and keep one installed copy. This draft does not require a global `AGENTS.md`, custom agent roster, or configuration changes. See [official skill documentation](https://learn.chatgpt.com/docs/build-skills) when packaging or installing.
