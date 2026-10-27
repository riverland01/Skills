# Grill Me

Clarify and stress-test complex ideas, plans, decisions, and uncertain briefs across research, strategy, career choices, creative work, processes, and technical projects.

| Target system | Complete skill | Entry point |
| --- | --- | --- |
| Codex | [codex/](codex/) | [SKILL.md](codex/SKILL.md) |
| Claude (Claude Code and Cowork) | [claude/](claude/) | [SKILL.md](claude/SKILL.md) |

**Codex:** copy the complete `codex/` folder into the skill location used by your Codex setup, with the destination folder named `grill-me`. Keep `agents/` and `references/` beside `SKILL.md`. Invoke it with `$grill-me` and the topic you want to examine. The [Codex package](releases/grill-me-codex.zip) contains that same skill under a `grill-me/` root folder.

**Claude Code:** copy the contents of `claude/` to `~/.claude/skills/grill-me/` (or `.claude/skills/grill-me/` inside a project), keeping `references/` beside `SKILL.md`. Start a new session and invoke it with `/grill-me` and the topic, or ask to be grilled.

**Cowork / Claude apps:** upload the [Claude package](releases/grill-me-claude.zip) in the Claude app's Skills settings, then enable it. It contains the `claude/` skill under a `grill-me/` root folder.

The Claude edition keeps the Codex behavior and changes only runtime bindings: no `agents/openai.yaml`, structured choices via `AskUserQuestion`, read-only subagents for delegation, Cowork's outputs folder as a record location, and an explicit ban on writing to Claude's memory or `CLAUDE.md`. Its [design-sources.md](claude/references/design-sources.md) records the adaptation.

## Behavior

- Adaptive questions: one at a time or small independent rounds, with structured choices when helpful.
- Evidence-grounded challenge, alternatives, failure checks, and prospective input requirements.
- A compact, revisable record of decisions, assumptions, deferred concerns, and next steps.
- Resumption and conversation-only checkpoints where files are unavailable.
- A handoff that respects the scope and authorization already given.

The skill combines five surveyed designs; [design-sources.md](codex/references/design-sources.md) records the retained strengths and deliberate tradeoffs. It has no mandatory question count or separate skill dependency.

## Verification

See the [verification record](verification/verification-2026-10-27.md), [historical coherence audit](verification/coherence-audit-2026-10-27.md), and [synthetic evaluation evidence](verification/grill-me-verification-evidence.zip). The two minor omissions identified in the audit were subsequently incorporated.

The six synthetic sessions covered the original revision. The two additions received focused diff, structural, package, and installed-file checks. The Claude edition received a diff review against the Codex edition and package-structure checks only; the synthetic sessions were not rerun on Claude. Alternate runtimes and every future interview behavior are not certified. Evidence paths are normalized for portability.
