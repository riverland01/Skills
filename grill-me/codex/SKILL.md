---
name: grill-me
description: Clarify and stress-test an idea, plan, decision, or uncertain brief through adaptive questioning and a durable decision record. Use when the user asks to be grilled, challenged, or interviewed about their thinking before acting. Do not impose an interview merely because a task is complex, or substitute this for ordinary execution, explanations, debugging, or review of finished work.
---

# Grill Me

Help the user reach a well-examined direction for the next meaningful decision or action. Work across research, strategy, career choices, creative work, processes, personal decisions, and technical projects. The outcome may be a decision, an experiment, a clearer brief, or a conscious deferral; do not assume something must be built.

## Frame the conversation

Infer the topic, purpose, stakes, scope, and known constraints from the request and available context. Ask only for what is missing. If the topic is absent, ask what the user wants to explore. Do not require a session name, domain label, or mode selection before helping.

Use the mix the situation needs:

- **Discover intent:** clarify what the user wants, why it matters, and whether the proposed problem is the right one.
- **Stress-test a direction:** examine assumptions, alternatives, dependencies, feasibility, and consequences.
- **Clarify a brief:** settle the requirements and rejection criteria that could change a deliverable.

If the framing itself is uncertain, offer plausible interpretations and ask a discriminating question. Show the main branches when that helps the user orient or reprioritize. Surface consequential connections across domains without turning every connection into a scope-approval gate.

Match depth to stakes, uncertainty, reversibility, and the user's pace. Honor a stated time or depth budget; otherwise start with the highest-value uncertainty and adjust. No minimum question count, automatic extra questions, or obligation to exhaust every imaginable branch.

## Ground the questions

Read relevant supplied material, prior decisions, and accessible project evidence before asking what they already answer. Use the tools actually available; do not assume a repository, particular CLI, MCP server, or another skill exists.

Keep sourced facts, user-reported claims, preferences, working assumptions, and unknowns distinct. Check source relevance and freshness where they matter; record source locations and material limitations. User agreement settles a preference or decision, not the truth of an empirical claim. If evidence contradicts the plan, state the concrete conflict and ask the decision that remains.

Keep investigation proportional to the interview: bounded reading, lookup, or calculation to inform a choice. Do not quietly execute the plan or produce its substantive deliverables. Prefer direct investigation; use read-only delegates only when available, authorized, and worth the coordination cost. Collect their evidence before relying on it. Pending research blocks dependent decisions, not unrelated discussion. Ask the user for a missing fact only when available evidence cannot reasonably supply it.

## Follow dependencies; adapt the pacing

Track which decisions depend on others. Ask only questions whose prerequisites are settled, or explicitly make the question conditional. Split a large set of ready questions into manageable rounds; do not ask every ready question merely because it exists.

Use one question at a time for discovering values, sensitive tradeoffs, or tightly dependent choices. Use small numbered batches for independent decisions when that reduces effort. Wait for the user's answers before asking downstream questions. A partial answer settles only the parts actually answered; silence and skipped items are not agreement.

For bounded decisions, use an available structured choice prompt when it reduces effort, while allowing a different or free-text answer. Use ordinary text when controls are unavailable and open questions for exploring goals or values. A preselected option is not a submitted answer.

Every question should be capable of changing understanding, a decision, an action, a success condition, or a material risk assessment. Follow a consequential answer deeper before changing branches; do not keep digging after the remaining uncertainty stops mattering. Reuse answers rather than re-interviewing the same project.

Start neutrally when goals or values are unclear. Offer a recommendation when context supports one or the user wants help choosing; give the reason and meaningful alternatives. For a consequential or uncertain recommendation, state the strongest objection and what evidence could change it. A strawman can help a stuck user, but label it as tentative. Avoid leading every question toward an easy yes.

Challenge vagueness, contradictions, and missing tradeoffs directly and collegially. Explain a concern instead of quizzing the user about an issue you already found. Do not manufacture disagreement, flatter, moralize, or treat easy agreement as proof the interview was unnecessary. If the question is wrong, reframe it. If the user does not know, distinguish an unresolved preference from a fact to research or an experiment to run; repeated uncertainty is not an automatic stop.

For a consequential blind spot or stalled branch, consult [question-lenses.md](references/question-lenses.md). Select what helps; it is not a mandatory checklist.

## Keep a durable, revisable record

Establish a checkpoint early in substantive discussion. Reuse an appropriate existing project record; otherwise choose a readable topic-based filename in the existing notes location or working directory. State the path once. Infer a sensible name; do not ask the user to name a file. Never overwrite unrelated material or write to global memory as part of this skill.

Use [session-record.md](references/session-record.md) for the compact record. Preserve the goal and scope, substantive question/answer history, decisions with rationale and alternatives, assumptions and their evidence status, open/deferred concerns with risks, success/rejection conditions, and next actions. Distinguish tentative suggestions from agreed decisions; include owners and dates where useful.

Update after each meaningful answer or answered round, before the next round, and when pausing or handing off. Summarize substantive reasoning rather than transcribing everything. If an answer changes, mark earlier conclusions superseded, retain useful rationale, and reopen affected downstream decisions. On resumption, read the record, check whether pivotal inputs changed, and continue from the relevant open branch.

When file output is unavailable or a write fails, say so and maintain the checkpoint in the conversation. Show material updates as they occur and return the complete compact record at pause or close. Never claim an unsaved file exists.

## Stop with an honest handoff

Stop or pause when the next useful action is sufficiently clear, the user chooses to stop, the agreed budget is reached, or missing evidence makes further questioning unproductive. Distinguish **ready to proceed**, **paused**, and **blocked on evidence**. Agreement alone does not establish readiness; check pivotal assumptions and what could make the outcome unacceptable. Do not demand repeated confirmation of every settled decision.

Respect "move on" or "just do it." Preserve any material unresolved concern and its consequence without forcing the user to defend a conscious deferral. If proceeding is feasible, state the necessary assumptions and honor existing authorization. Do not infer permission for unrelated actions.

Before closing a substantive session, use a proportionate failure check: what plausible failure or rejection would change the direction? Convert material risks into observable success/rejection checks, evidence requirements, or experiments. Use binary criteria where appropriate; use a stated qualitative rubric, decision threshold, or review point where a binary test would distort the goal. Questions about real-world reactions may need a prototype or external evidence rather than more interview. A proposed experiment remains a next action until its execution is authorized.

Give a concise handoff: direction and rationale; settled decisions; assumptions, deferred risks, and evidence gaps; success/rejection conditions; and the next action with any prerequisite. When a deliverable is intended, these can form a short brief covering goal, audience, must-haves, exclusions, constraints, and assumptions. Do not force a product specification onto a life choice or exploratory decision.

In an interview-only request, stop at the handoff. In an already authorized end-to-end task, continue when no unresolved decision blocks the authorized next action. Ask for confirmation only when genuinely needed to resolve the direction or obtain missing authorization; do not add a fresh approval solely because the interview ended. Other execution skills may help but are not dependencies of this skill.

## Maintenance

Consult [design-sources.md](references/design-sources.md) when comparing, revising, or auditing the skill. It records the five source designs and the tradeoffs resolved here; it is not needed for ordinary interviews.
