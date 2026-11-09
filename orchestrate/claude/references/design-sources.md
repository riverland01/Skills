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

## Claude Code adaptation (2026-10-20)

Adapted from the shortened portable `orchestrate` draft (19 Oct 2026):

- `AGENTS.md` references replaced with `CLAUDE.md`.
- Codex-only `agents/openai.yaml` dropped; Claude Code reads only `SKILL.md` frontmatter.
- Added a "Claude Code mechanics" section mapping workers, parallel dispatch, follow-ups, cancellation, isolation, and verifiers onto `Agent`, `SendMessage`, `TaskStop`, `isolation: "worktree"`, and the opt-in-only Workflow tool.
- Description rewritten for clearer auto-invocation triggers.
- Core coordination rules otherwise kept verbatim to preserve the original rule-preservation review.

## Model and effort scaling (2026-11-09)

Ported from upstream commit `b14f317` ("Scale Orchestrate model and reasoning effort to task complexity", riverland01/Skills):

- Added the "Match model and effort to the task" section, keeping the upstream wording and adding Claude Code examples (`model: "haiku"`, `effort: "low"`; omit both for the default).
- Rewrote the `Workers` mechanics bullet to point to that section, note that this skill is the explicit instruction the `Agent` tool's `effort` parameter requires, and note that forks ignore both overrides.

Install as a personal skill at `~/.claude/skills/orchestrate/` (or `.claude/skills/orchestrate/` inside a project). See the [Claude Code skills documentation](https://code.claude.com/docs/en/skills).
