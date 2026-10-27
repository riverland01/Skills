# Grill-me coherence and five-source coverage audit

Status update: F1 and F2 were subsequently incorporated into the installed skill and download package at the user's request. The audit below records the original revision and its original line numbers; it is retained as historical evidence. Current verification is in `verification-2026-10-27.md`.

Date: 2026-10-27
Scope: read-only review of the installed skill, delivered copy, and all five upstream instruction designs. The skill and its existing archive were not changed.

## Conclusion

The content is internally coherent and retains the main strengths of all five designs. Two useful details were omitted as explicit instructions: native choice controls for bounded questions, and a lens for the inputs a future task will require. These are minor coverage gaps, not blockers or contradictions. The earlier description that the skill combined every useful detail was too broad.

## Evidence and method

- Read the entrypoint, three references, and interface metadata.
- A fresh source-coverage reviewer read all five complete primary designs plus Matt Pocock's wrapper, independently of the previous audit.
- A separate fresh reviewer assessed internal coherence without reading the prior conclusions.
- Root checked the reported gaps against the actual upstream passages and current candidate text.
- Confirmed that all five installed files match the delivered copy, and that the existing skill archive matches that copy.
- Entrypoint SHA-256: `b593d5b299d2e32c3c60c0eecb84efefaa0ac1767fcf23a1cc45fa4d4a4dddd6`.

The prior structural and behavioral checks were not rerun: the skill bytes are unchanged, and this request concerns instruction coherence and source coverage. This audit adds static evidence, not a new live-interview result.

## Findings

### F1 — Native choice prompts were omitted

[Tsudo](https://github.com/tsudo/skills/blob/main/skills/grill-me/SKILL.md#L84) and [kshyam](https://github.com/kshyam/opencode-and-claude-skills/blob/main/grill-me/SKILL.md#L27) explicitly use available interactive controls for bounded choices. The combined skill describes pacing and recommendations at `SKILL.md:36–40`, but gives no corresponding tool-selection guidance. Its generic instruction to use available tools does not specifically retain this convenience.

Impact: an interview may require typed answers when a simple selection would reduce effort. The capability is not prohibited; it is no longer prompted reliably.

Suggested narrow addition to the pacing section: use the runtime's structured choice prompt for a bounded decision when it helps; retain an open-answer route and use ordinary text when controls are unavailable. This should not make recommendations mandatory or turn exploratory questions into forced choices.

### F2 — Future input requirements are under-specified

[Kshyam](https://github.com/kshyam/opencode-and-claude-skills/blob/main/grill-me/SKILL.md#L52) explicitly probes integrations and content/data requirements. Reading supplied evidence at `SKILL.md:26` is a different operation: it establishes what exists now, rather than what later work will need. Neither the question-lens table nor the short brief explicitly restores that future-input check.

Impact: a brief can establish the goal and audience while leaving input availability, representation, examples, scale, or necessary connections unclear. This is most relevant to research, analysis, documents, workflows, and software that depend on external material.

Suggested narrow addition to the lenses: when the outcome depends on inputs, ask where they will come from, whether they are available, what form and scale they have, and what connection or example is necessary to establish feasibility. Apply only where consequential.

## Strength coverage

Line numbers refer to the unchanged files under `grill-me/`.

| Source | Strength | Current evidence | Assessment |
| --- | --- | --- | --- |
| [Matt Pocock](https://github.com/mattpocock/skills/blob/main/skills/productivity/grilling/SKILL.md) | Decision prerequisites and ordered discussion | SKILL.md:34–36 | Retained |
| Matt Pocock | Research facts; leave choices to the user | SKILL.md:28–30,40 | Retained |
| Matt Pocock | Pending research does not block unrelated branches | SKILL.md:30 | Retained |
| Matt Pocock | Shared understanding before action | SKILL.md:58,64–66 | Retained with existing-authorization handling |
| [satya-janghu](https://github.com/satya-janghu/agent-skills/blob/main/skills/grill-me/SKILL.md) | Discover intent and challenge the framing | SKILL.md:16,20 | Retained |
| satya-janghu | Follow consequential answers deeply; reframe poor questions | SKILL.md:38–42 | Retained |
| satya-janghu | Alternatives, values, assumptions, reversibility, sustainability | question-lenses.md:7–18 | Retained in adapted language |
| satya-janghu | Distill decisions and reasoning | SKILL.md:50–52; session-record.md:13–33 | Retained |
| [stevegsax](https://github.com/stevegsax/grill-me/blob/main/SKILL.md) | Collegial disagreement and scope awareness | SKILL.md:20,42 | Retained |
| stevegsax | Decisions, unresolved risks, and conscious deferral | SKILL.md:50,60; session-record.md:13–25 | Retained |
| stevegsax | Resume, reopen, and correct earlier conclusions | SKILL.md:52 | Retained |
| stevegsax | Separate discussion from execution | SKILL.md:30,66 | Retained with explicit end-to-end exception |
| [tsudo](https://github.com/tsudo/skills/blob/main/skills/grill-me/SKILL.md) | Clarify problem shape and follow dependencies | SKILL.md:20,34 | Retained |
| tsudo | Checkpoints and conversation fallback | SKILL.md:48–54 | Retained |
| tsudo | Objection to uncertain recommendations | SKILL.md:40 | Retained |
| tsudo | Experiments, failure checks, usable criteria | SKILL.md:42,62 | Retained; qualitative evaluation permitted |
| tsudo and kshyam | Available structured choices | No specific instruction | Minor omission: F1 |
| [kshyam](https://github.com/kshyam/opencode-and-claude-skills/blob/main/grill-me/SKILL.md) | Outcome-changing questions and context reuse | SKILL.md:26,38 | Retained |
| kshyam | Rejection conditions, manageable rounds, useful brief | SKILL.md:36,58,64 | Retained |
| kshyam | User escape hatch and reduced repeat questioning | SKILL.md:38,60,66 | Retained |
| kshyam | Prospective input requirements | Only generic evidence/constraint guidance | Partial: F2 |

## Coherence checks

No material contradiction was established in these interactions:

- **One question versus batches:** the skill distinguishes sensitive or dependent choices from independent decisions.
- **Neutral inquiry versus recommendations:** discovery starts neutrally; advice is conditional on sufficient context or a request for help choosing.
- **Research versus execution:** bounded investigation informs decisions; substantive execution follows the separate handoff rule.
- **Stop versus continue:** interview-only work ends at the handoff; existing end-to-end authorization can continue once its blocking decisions are settled.
- **Durability versus brevity:** substantive reasoning and corrections are recorded without requiring a transcript.
- **Uncertainty versus readiness:** proposed ideas, empirical claims, preferences, and open risks remain distinguishable; agreement does not make a factual claim true.
- **General tasks versus product briefs:** a decision or experiment can be the outcome; a deliverable brief is conditional.

## Deliberate changes, not missed strengths

The combined skill intentionally avoids compulsory question counts, automatic extra questions, whole-frontier batches, mandatory recommendations, exhaustive hypothetical coverage, a ban on useful summaries, forced binary criteria, mandatory delegation, repeated approval gates, and product specifications for every topic. Restoring these source rules wholesale would bring back the drawbacks the synthesis was meant to reduce.

Dedicated source labels such as a parking lot, a separate completed state, or named mental models were not copied verbatim. The substantive behaviors are supported by open/deferred records, handoff states, and adapted questioning lenses. Their different wording alone is not evidence of lost function.

## Recommendation and limits

Add F1 and F2 as two short, conditional instructions. A rewrite or extra workflow layer is not warranted by this audit. No skill changes were made.

These are static source-to-instruction findings. They do not establish that every future agent will use all retained strengths. Upstream main-branch links are mutable, and the audit does not reconstruct an immutable historical upstream revision.
