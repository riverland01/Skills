# Design sources

These references informed the original design. They are optional maintenance resources, not runtime dependencies. Inspect current upstream instructions before adapting further material; preserve this skill's selective, cross-domain scope.

| Source | Adopted pattern |
| --- | --- |
| [OpenAI Codex orchestrator template](https://github.com/openai/codex/blob/main/codex-rs/core/templates/agents/orchestrator.md) | Root coordination, independent parallel work, waiting, avoiding duplication. |
| [OpenAI code-review routing](https://github.com/openai/codex/blob/main/.codex/skills/code-review/SKILL.md) | Fan out across relevant dimensions and aggregate findings. |
| [OpenAI research routing](https://github.com/openai/plugins/blob/main/plugins/life-science-research/skills/research-router-skill/SKILL.md) | Normalize scope, delegate evidence gathering, retain conflict resolution and synthesis at the root. |
| [Gentle-AI](https://github.com/Gentleman-Programming/gentle-ai) | Dependency-aware handoffs, collection and artifact checks, capability-aware fallback. Software-specific phases are not mandatory here. |
| [provencher/codex-skills — orchestrate](https://github.com/provencher/codex-skills) | Compact contracts, distinct ownership, leaf workers, parent integration. |
| [Superpowers](https://github.com/obra/superpowers) | Focused contexts and independent review. Fixed software-development ceremonies are not adopted. |

## Antigravity adaptation (2026-11-22)

Adapted from the hardened `orchestrate/codex/SKILL.md` (commit `d5a61e3`, `riverland01/Skills`):

- Replaced `AGENTS.md`-only project rule reference with Antigravity's `GEMINI.md`, `AGENTS.md`, and `.agents/rules/*.md`.
- Dropped Codex-only `agents/openai.yaml`; Antigravity discovers `skills/<name>/SKILL.md` frontmatter.
- Added an "Antigravity mechanics" section mapping workers, parallel dispatch, follow-ups, cancellation, workspace isolation, model selection, and compaction continuity onto `invoke_subagent`, `define_subagent`, `send_message`, `manage_subagents`, `Model` (`flash_lite`, `flash`, `inherit`, `pro`), `Workspace` (`inherit`, `share`, `branch`), and `<Artifact Directory Path>/scratch/`.
- Added explicit escalation boundaries for `run_workflow` (programmatic high-count fan-outs) and `swarm` / `native_swarm` (deferring to `native_swarm` rules whenever a Swarm is already active, including its model-pinning policy).
- Core coordination rules otherwise kept aligned with the Codex edition.

Install globally at `~/.gemini/config/skills/orchestrate/` (or per-workspace at `.agents/skills/orchestrate/`). See the [Antigravity Skills documentation](https://antigravity.google/docs/skills).
