# Grill-me verification

Date: 2026-10-27
Result: created, validated, packaged, installed, and updated after the coherence audit.

## Current update

The installed skill now uses available structured choice prompts for bounded decisions when helpful, with a free-text route and ordinary-text fallback. Its optional lenses now cover prospective input sources, availability, formats, examples, scale, and integrations.

The update added one instruction paragraph and one lens row, with corresponding source-map edits. The exact diff was reviewed; interface metadata and session-record guidance are byte-for-byte unchanged. The official validator passed on both the candidate and installed copies. Encoding, references, YAML, archive integrity, and installed five-file hash/byte equality also passed.

The six synthetic sessions below were performed on the original revision and were not repeated for these narrow additions. The existing verification-evidence archive preserves those original session artifacts and manifests. Current package and entrypoint hashes are recorded at the end of this report.


## Delivered skill

- Entry point: `../codex/SKILL.md` (approximately 1,300 words).
- Optional question lenses, compact session-record guidance, and five-source design mapping.
- Codex interface metadata; normal automatic discovery remains enabled.
- No sibling skill, script, external server, or repository is required for an interview.
- Installed at `${CODEX_HOME}\skills\grill-me` after filesystem permission was granted.

## Source coverage and independent review

The design mapping in `grill-me/references/design-sources.md` records retained strengths and deliberate rule changes for Matt Pocock, satya-janghu, stevegsax, tsudo, and kshyam.

A dedicated synthesizer reviewed the complete candidate against all five sources. It found no material lost strength or contradictory requirement. One clarification was accepted: authorized work may continue when no unresolved decision blocks the next action, rather than requiring every material issue to be resolved. This permits useful progress with conscious deferrals.

The root checked the mapping and the evaluator artifacts. Agreement between agents was not treated as proof of source accuracy or future behavior.

## Controlled behavioral exercises

Three independent evaluation agents exercised six synthetic sessions. These were actual agent responses and, where applicable, actual local checkpoint writes; they were not live interviews with the human user.

| Session | Observed behavior |
| --- | --- |
| Career decision, three turns | Asked a manageable neutral question without forcing a deliverable. Kept an unanswered sub-question open. Marked a research-time expectation as unchecked. On correction, superseded that assumption and the prior interpretation of the user's values, reopened dependent conclusions, and paused without selecting a role. |
| Already-authorized reading-group checklist | Used the complete brief to create the local plain-text checklist immediately. Used placeholders, included three discussion prompts, and required no additional interview or approval. |
| Workshop atmosphere, no writable surface | Returned a complete conversation checkpoint, recorded the pause and evidence gap, and proposed external evaluation as an unexecuted next step. No runtime checkpoint file was created for that session. |
| Reading-club expansion after two uncertain answers | Reframed around a concrete meeting experience and continued one question at a time; did not stop automatically or invent a target scale. |
| Retreat with only one answered item | Recorded the stated budget, retained travel and venue as unanswered, and asked about attendee count before venue selection. |
| Fresh-context resumption | A fresh agent read the saved career checkpoint, preserved the corrected mentoring priority and superseded research-time assumption, and resumed with a relevant question. It left the original checkpoint unchanged. |

The file artifacts for these exercises, plus the source and installation manifests, are preserved in `grill-me-verification-evidence.zip`. The chat-only checkpoint is described above; it was deliberately not created as a runtime file.

## Structural and installation checks

All passed:

- Official `skill-creator/scripts/quick_validate.py`, on the output copy and the installed copy.
- Genuine PyYAML 6.0.3 parsing of the skill frontmatter and interface metadata.
- UTF-8 decoding, no byte-order marks, and all local Markdown reference targets.
- Interface description length and default automatic-discovery policy.
- ZIP CRC, unique members, safe relative paths, and byte equality with all five source files.
- Installed file-set equality, SHA-256 equality, and byte-for-byte read-back for all five files.

PyYAML was installed only into this task's intermediate working directory for validation; it is not a skill runtime dependency. Installation added the new `grill-me` directory and did not replace an existing skill.

## Limits

These checks establish instruction coverage and observed behavior in the stated synthetic cases. They do not prove performance for every future interview. Native skill discovery in a newly opened chat, alternate agent runtimes, a real checkpoint-write failure, external research/delegation, and exhaustive high-stakes decision quality were not tested. The chat-only exercise simulated the absence of a writable surface. Source links are mutable upstream URLs, dated to this review.

## Integrity

- `../releases/grill-me-codex.zip` SHA-256: `0ca958d28d0a78d16898826b59964f7c569644ed3fe1c86d49810a205b0c7678`
- `../codex/SKILL.md` SHA-256: `c678edbfa35805a7ce92b48302b81f80e0b7a5a2657ea1d6d5f0ab4a1f86b1de`

## Repository publication

The published skill files and release ZIP preserve the validated installed-package bytes. Machine-specific paths in this report and the evidence archive are replaced with `${CODEX_HOME}` or `${WORKSPACE}` for portability. The evidence archive retains the original synthetic session records and original manifests, plus the current additions and installed-file manifests under `update/`. It contains no real career decision or participant data.
