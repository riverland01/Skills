# Orchestrate

Coordinate complex research, analysis, documents, strategy, and software work through selective delegation, synthesis, and verification.

| Target system | Package | Entry point |
| --- | --- | --- |
| Codex | [codex/](codex/) | [SKILL.md](codex/SKILL.md) |
| Claude Code | [claude/](claude/) | [SKILL.md](claude/SKILL.md) |

**Codex:** the `codex/` folder is the complete skill: keep `SKILL.md`, `agents/`, and `references/` together. When installing it, copy that folder into the supported skill location with the destination folder named `orchestrate`.

**Claude Code:** copy the contents of `claude/` to `~/.claude/skills/orchestrate/` (or `.claude/skills/orchestrate/` inside a project), keeping `references/` beside `SKILL.md`. Start a new session and invoke it with `/orchestrate`, or let it trigger on matching tasks.

The [design sources](codex/references/design-sources.md) describe its influences and scope. Both editions favor lighter models or lower reasoning effort for bounded assignments when the runtime supports those choices.

The Claude edition keeps the Codex coordination rules and changes only runtime bindings: `CLAUDE.md` instead of `AGENTS.md`, no `agents/openai.yaml`, a "Claude Code mechanics" section mapping workers, follow-ups, cancellation, isolation, and verifiers onto `Agent`, `SendMessage`, `TaskStop`, worktree isolation, and the opt-in-only Workflow tool, and concrete `model`/`effort` settings for the model-and-effort section. Its [design-sources.md](claude/references/design-sources.md) records the adaptation.

See the shared [verification record](../docs/verification-2026-10-19.md) for review coverage and limits. The Claude edition received a diff review against the Codex edition only; the original review was not rerun on Claude.
