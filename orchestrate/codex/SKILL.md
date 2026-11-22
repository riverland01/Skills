---
name: orchestrate
description: Coordinate complex work across research, analysis, documents, strategy, and software through adaptive decomposition, subagents, synthesis, and verification. Consider this skill for tasks with 2+ independently answerable workstreams, 2+ distinct evidence types or capabilities to reconcile, or 3+ substantive steps with dependencies; a single consequential uncertainty may also warrant it. These are guideposts, not requirements or automatic delegation triggers. Delegate only when expected quality and context-management benefits justify total coordination cost; counts of steps, files, or sources and task length alone do not establish complexity.
---

# Orchestrate

Adapt coordination across domains; impose no coding pipeline, fixed roster, agent count, or review ceremony. The user supplies the objective and preferences; applicable project `AGENTS.md` files supply context. Do not create or require a user-level `AGENTS.md` or project activation rule. Respect higher-priority instructions.

## Frame and choose coordination

Establish the objective, deliverable, constraints, and completion evidence before substantial work. Separate fixed requirements from challengeable assumptions. Explore briefly before decomposing an unclear problem; revisit framing when findings undermine it. Open-ended acceptance may be supported options with explicit uncertainty.

First consider direct execution or one suitable specialist skill/tool. Delegate only when quality and context-management benefits justify briefing, duplicated reading, tools, waiting, integration, and review. Apply this qualitative test to each worker, follow-up, and review, even when explicitly invoked. Size, speed, domain labels, and capacity alone are insufficient; sequential independent review can help. Preserve required evidence/checks and do not invent token estimates. Explain consequential coordination decisions without an approval ceremony.

Use actual native capabilities and limits; assume no tool names, model options, access, isolation, or shared files. If concurrent parent work is required, satisfy that condition for every dispatch without busywork. Without delegation, execute dependencies directly and disclose missing independent agent verification when material. Do not simulate agents or substitute user-visible chats.

## Match model and effort to the task

Choose the least resource-intensive model and reasoning effort likely to meet the acceptance criteria for each assignment, including reviews. Use the task's ambiguity, consequences of error, and ease of checking the result to make that choice.

- Handle straightforward work directly when delegation would add overhead. For bounded assignments with clear inputs and easy checks, prefer a lighter model or lower reasoning effort.
- Use the runtime default for ordinary synthesis or implementation. Use a more capable model or higher effort for consequential judgments, conflicting evidence, or work that is hard to verify. Keep routine subtasks lightweight even within a complex project.
- Reassess at checkpoints. Raise effort or capability for the affected work when uncertainty, a failed check, or unexpected complexity warrants it. Reuse accepted results and keep required verification in scope.

Honor user and project settings. Apply model or effort overrides only where the runtime supports and permits them. Otherwise keep the configured settings and control cost through focused scope and concise context.

## Track tasks and acceptance

Scale tracking: a single assignment needs a tracked return; dependent work needs a compact graph. Record task ID/objective, prerequisites/inputs, owner/scope including permitted writes, expected output/acceptance, and state: pending, running, completed, blocked, failed, or cancelled. Keep tightly coupled work together; use a scout only when missing context prevents decomposition. Revise the graph as evidence changes. For multi-wave or extended runs, persist the compact task graph, criterion ledger, and artifact index in an accessible state/scratch file so the root can recover cleanly after context compaction or interruption.

For substantial work, track criterion ID, responsible task IDs or root-owned work, status, and evidence/gap alongside that graph. Simple work needs a checklist. Criterion states differ from task states: **unverified** = not established; **met** = sufficient current evidence inspected and accepted by the root; **unmet** = checked but unsatisfied; **blocked** = assessment prevented by missing prerequisites/evidence. Worker completion alone establishes no acceptance.

Choose workers by actual capabilities; roles confer neither expertise nor access. Name workers functionally (`parser`, `pricing-audit`, `verifier`), not opaque IDs; for homogeneous batch slices, factor shared rules into one template with per-slice targets. Assign mutable-resource ownership, including files, browser sessions, workbooks, databases, and account state. Keep read-only workers and verifiers off write ownership (verifiers report findings; authors fix). For concurrent writers, assign disjoint resources, serialize conflicting operations, or use verified workspace isolation (such as worktrees or branches): verify the isolated base state (committed head vs. uncommitted changes) and land accepted changes (commit, merge, cherry-pick, or export) before cancelling or discarding the worker/workspace. Use applicable specialist skills for execution and validation; pass their locations/purpose and project rules rather than reproduce their procedures.

## Brief workers

A fresh worker sees none of this conversation and will invent unstated context. Share relevant definitions, source versions, assumptions, and comparison criteria; state explicit `must not touch` boundaries alongside permitted changes. Distinguish user preferences, supplied claims, and established facts; authority for an edit does not establish factual accuracy. Start cold when independence matters (verification, replacing a looping worker); prefer focused follow-ups or forked/warm context (where supported) when branching a deep investigation or continuing tightly coupled work. Pass concise excerpts and primary artifact locations or message IDs rather than paraphrasing another worker's report or dumping whole histories; preserve material qualifications and allow needed retrieval.

Adapt this contract:

> **Objective:** bounded question or artifact.  
> **Inputs:** requirements, prerequisite artifact locations, sources/versions, applicable rules.  
> **Scope:** owned resources, permitted changes, must not touch, available tools, constraints.  
> **Acceptance:** criterion IDs when tracked, output, evidence, completion checks.  
> **Return:** status; findings/changes mapped to criteria; evidence/artifact locations; checks/results; gaps/blockers and next action. On follow-up, report changes since the previous return.  
> **Delegation:** remain a leaf unless the root explicitly assigns bounded further decomposition with ownership and a collection path.

Distinguish no findings from not checked, inaccessible sources, and incomplete coverage. Keep necessary detail in accessible artifacts; omit repeated background/raw logs. Briefs inherit authorization and grant no unrelated external actions.

## Dispatch, collect, and refresh

Dispatch ready independent work within capacity. Keep root-side complementary work bounded and interruptible (framing, judgment, light synthesis, small glue edits) without duplicating worker effort, and delegate heavy builds, bulk reads, or large edits so the root stays responsive to completions, stalls, and user steering while preserving integration context. Before releasing a dependent task, collect and inspect every prerequisite against acceptance, including artifact existence. A worker saying "done" is insufficient. Independent branches may continue while others wait. Where the runtime supports shared channels or peer messaging, address only the next actor that must wake rather than broadcasting routine status.

Reuse accepted evidence with locations, versions, and limitations; refresh for scope, freshness, contradictions, or verification. Summaries do not become authoritative through reuse.

Track every worker through collection or confirmed cancellation. Do not cancel idle workers that cost nothing if follow-up is likely. When cancelling or tearing down a worker, use supported lifecycle controls, land any accepted changes from isolated workspaces first, confirm stopped operations, stop or collect any child workers it spawned under sub-delegation, and inspect partial changes before retrying, transferring ownership, or finalizing affected artifacts. Incorporate user steering into active contracts. Never leave an uncollected worker changing a final deliverable.

When inputs, requirements, or assumptions change, mark dependent outputs stale, reopen affected criteria as unverified/blocked, and update active workers. Refresh only affected work, preserve unaffected results, and check derived artifacts against current inputs before finalization.

## Reassess effort and recover

For extended work, identify the next meaningful checkpoint: collection, integration, or focused recovery. Reassess before material expansion, after significant replanning, and near explicit user/runtime limits. Assess evidence gained, remaining criteria, applicable limits/observable effort, and the gap the next action would resolve. Continue, correct, replan, or finish directly using the delegation cost-benefit test; briefly explain material changes.

Checkpoints are internal decisions, not routine approval pauses or reasons to abandon unfinished work. Preserve scope, acceptance, and required checks. Respect hard limits and report unresolved criteria if they prevent completion; continue useful unaffected work where feasible.

Handle both explicit and silent failures by assessing cause, dependencies, ownership, and verified partial results while keeping dependents blocked:

- **Explicit or partial failure:** supply missing context, use an available source/tool alternative, narrow/split assignments, serialize interference, request targeted evidence, or complete directly. Stop a failed branch with alternatives when recovery is infeasible. Retry only with a plausible changed condition; never repeat unchanged failure. Update contracts/graph and recheck recovered outputs without duplicating side effects.
- **Stalls and loops:** distinguish healthy long-running work (builds, deep searches—wait) from looping/non-converging workers (interrupt, inspect partial state, and replace with a fresh worker and narrower scope) and stalled/unresponsive workers (re-ping once, then escalate, fallback, or reassign).
- **Quota or rate limits:** if a worker hits quota or capacity limits, switch or downgrade its model in-place when the runtime preserves its conversation rather than discarding accumulated work; notify the user if capability materially degrades.

Notify the user when failure materially affects quality, timing, scope, or deliverables, stating impact and revised approach/trade-offs. Routine authorized recovery proceeds directly. Seek a decision only for new authorization or consequential unaccepted trade-offs; otherwise report precise blockers, completed work, and alternatives.

## Integrate, verify, and finish

The root owns framing, evidence weighting, conflict resolution, integration, and judgment. Distinguish facts, assumptions, and inferences; resolve disagreement with evidence/follow-up rather than voting. Deliver a coherent result, not concatenated reports. For mid-flight user updates on extended runs, group status by deliverable/outcome (blocked, active, done) rather than an agent-by-agent log, and clearly separate internal recovery from user decisions.

Use a separate verifier when the particular claim's consequences, uncertainty, or integration risk warrant it; domain significance alone does not justify reviewing every minor edit. Give original requirements and relevant primary evidence/artifacts without seeding the conclusion. Verifiers inspect and report; authors fix. Self-checks alone cannot satisfy required independent verification.

Choose checks suited to the claim through specialist methods. Fresh agents can share mistaken assumptions: seek independent evidence/methods where material, such as primary-source inspection, recalculation, counterexamples, rendering, or behavioral tests. Agent agreement alone is not verification. Inspect integration where it can introduce errors; fix material findings and recheck affected work. Distinguish self-checks from unavailable independent checks. Reuse primary evidence for separate assessment; do not repeat passed checks without a material reason or expand review without the cost-benefit test.

Before claiming completion, collect all dispatched outputs or confirm cancelled workers (and any sub-delegates) have stopped; land any isolated workspace changes, inspect partial changes, satisfy dependencies/checks, and reconcile findings and required criteria against the current integrated result. Stop when completion evidence is satisfied. Report results, verification, limitations, and material unmet/blocked/unverified criteria. Distinguish success from hard-limit or blocker stops; blocked prerequisites cannot become success claims.

## Failure modes to design out

- **Write collisions:** two workers modifying the same file or mutable resource, or a verifier editing an author's files.
- **Cold-start invention:** omitting decisions, definitions, or `must not touch` boundaries from a fresh worker's brief.
- **Telephone-game drift:** paraphrasing one worker's report into another's brief instead of passing primary artifact locations.
- **Compaction amnesia:** keeping a multi-wave task graph and criterion ledger only in conversation memory.
- **Unlanded teardown:** cancelling or discarding an isolated workspace/worktree before landing its accepted changes.
- **Orphaned sub-delegates:** cancelling a delegating worker while leaving its child workers running.
- **Silent stall or quota thrash:** letting a looping worker burn turns, or killing a quota-limited worker whose state could be preserved.
- **Rubber-stamp verification:** treating worker completion, self-checks, or agreement among similarly primed agents as proof.

## Design reference

For maintenance, consult [design-sources.md](references/design-sources.md). Routine use requires neither loading nor installing those references.
