# Design sources and synthesis

Reviewed: 2026-10-27. This is an original synthesis of the instruction designs below, not a claim that every source rule can coexist. Links target mutable upstream files; the date identifies the review, not an immutable source version. No upstream code or full skill text is bundled. The combined skill is self-contained.

| Source | Strengths retained | Rules changed or omitted |
| --- | --- | --- |
| [Matt Pocock: grilling](https://github.com/mattpocock/skills/blob/main/skills/productivity/grilling/SKILL.md), reached through [grill-me](https://github.com/mattpocock/skills/blob/main/skills/productivity/grill-me/SKILL.md) | Follow prerequisite decisions; investigate facts; keep user decisions with the user; continue independent branches while research is pending; seek shared understanding. | Small adaptive rounds replace asking the entire ready frontier. Qualified recommendations replace universal yes-oriented wording. Delegation is selective, not mandatory. No wrapper or sibling-skill dependency. Readiness depends on material decisions, rather than every conceivable branch. |
| [satya-janghu: grill-me](https://github.com/satya-janghu/agent-skills/blob/main/skills/grill-me/SKILL.md) | Discover intent, values and constraints; follow significant answers deeply; consider alternatives, reversibility and failure; reframe poor questions; preserve reasoning. | Omit automatic extra questions and the ban on useful summaries. Add ongoing checkpoints. Recommendations are optional during discovery. Discovery and feasibility examination are distinct but available in the same interview. |
| [stevegsax: grill-me](https://github.com/stevegsax/grill-me/blob/main/SKILL.md) | Collegial challenge; scope awareness; visible branches; decisions with rationale; deferred risks; resumption and reopening; separation of interviewing from performing the task. | Infer filenames and scope instead of mandatory setup questions. Surface relevant cross-domain implications without repeated gates. Use available tools. Respect existing end-to-end authorization at handoff. The source repository was archived when reviewed. |
| [tsudo: grill-me](https://github.com/tsudo/skills/blob/main/skills/grill-me/SKILL.md) | Clarify the problem's shape; order dependencies; investigate evidence; checkpoint rounds; state objections to uncertain recommendations; flag experiments; translate failure into usable checks; support chat-only operation and native choice prompts where helpful. | No universal question limit or stop after two uncertain answers. Agreement is not proof of clarity or uselessness. Limit batch burden. Qualitative goals can use rubrics or review points rather than forced binary criteria. Avoid required jargon. |
| [kshyam: grill-me](https://github.com/kshyam/opencode-and-claude-skills/blob/main/grill-me/SKILL.md) | Ask questions that change the outcome; reuse context; cover rejection criteria, lifecycle, future inputs and integrations; offer structured choices, manageable rounds and a brief; honor a request to proceed; avoid repeat interviews. | No automatic interview for every complex request, no mandatory 10–15 questions, and no universal product-spec outcome. Separate understanding from authorization, preserving authorization already given. Use valid, self-contained metadata and durable checkpoints. |

## Reconciled tradeoffs

- Depth and speed: prioritize uncertainties that can change the decision, scale depth to stakes and user pace, and allow conscious deferral.
- Helpfulness and anchoring: begin neutrally when intent is unclear; use reasoned, provisional recommendations when context supports them.
- Continuity and overhead: keep a compact decision record with substantive reasoning; avoid transcripts and constant full-record repetition.
- Planning and action: bounded investigation informs questions; actual execution follows the user's existing scope and authorization.
- Rigor and uncertainty: distinguish empirical claims from choices, preserve limitations, and use experiments when discussion cannot provide evidence.
- Generality and focus: use domain-appropriate lenses without forcing product development, technical tools, or a fixed checklist.

Instruction coverage and behavioral checks are recorded separately in the delivered verification report. They support this version's tested behavior; they do not guarantee all future model or runtime behavior.

## Claude adaptation

Ported from the Codex edition on 2026-10-27 for Claude Code and Cowork. Behavior is unchanged; only runtime bindings differ: `agents/openai.yaml` is dropped (Claude reads `name`/`description` from `SKILL.md` frontmatter), structured choices name `AskUserQuestion`, delegation names read-only subagents under the session's own rules, the record location includes Cowork's outputs folder, and the no-global-memory rule names Claude's memory and `CLAUDE.md`. Invoke with `/grill-me <topic>` or by asking to be grilled.
