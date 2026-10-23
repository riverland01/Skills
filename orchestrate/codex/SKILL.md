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

## Track tasks and acceptance

Scale tracking: a single assignment needs a tracked return; dependent work needs a compact graph. Record task ID/objective, prerequisites/inputs, owner/scope including permitted writes, expected output/acceptance, and state: pending, running, completed, blocked, failed, or cancelled. Keep tightly coupled work together; use a scout only when missing context prevents decomposition. Revise the graph as evidence changes.

For substantial work, track criterion ID, responsible task IDs or root-owned work, status, and evidence/gap alongside that graph. Simple work needs a checklist. Criterion states differ from task states: **unverified** = not established; **met** = sufficient current evidence inspected and accepted by the root; **unmet** = checked but unsatisfied; **blocked** = assessment prevented by missing prerequisites/evidence. Worker completion alone establishes no acceptance.

Choose workers by actual capabilities; roles confer neither expertise nor access. Assign mutable-resource ownership, including files, browser sessions, workbooks, databases, and account state. Serialize conflicting operations unless isolation is verified; reviewers can inspect without editing ownership. Use applicable specialist skills for execution and validation; pass their locations/purpose and project rules rather than reproduce their procedures.

## Brief workers

Share relevant definitions, source versions, assumptions, and comparison criteria. Distinguish user preferences, supplied claims, and established facts; authority for an edit does not establish factual accuracy. Pass concise excerpts and accessible source locations, preserving material qualifications; allow needed retrieval rather than dumping whole histories.

Adapt this contract:

> **Objective:** bounded question or artifact.  
> **Inputs:** requirements, prerequisite outputs, sources/versions, applicable rules.  
> **Scope:** owned resources, permitted changes, available tools, constraints.  
> **Acceptance:** criterion IDs when tracked, output, evidence, completion checks.  
> **Return:** status; findings/changes mapped to criteria; evidence/artifact locations; checks/results; gaps/blockers and next action. On follow-up, report changes since the previous return.  
> **Delegation:** remain a leaf unless the root explicitly assigns bounded further decomposition with ownership and a collection path.

Distinguish no findings from not checked, inaccessible sources, and incomplete coverage. Keep necessary detail in accessible artifacts; omit repeated background/raw logs. Briefs inherit authorization and grant no unrelated external actions.

## Dispatch, collect, and refresh

Dispatch ready independent work within capacity; the root coordinates and performs complementary work without duplication. Before releasing a dependent task, collect and inspect every prerequisite against acceptance, including artifact existence. A worker saying "done" is insufficient. Independent branches may continue while others wait.

Reuse accepted evidence with locations, versions, and limitations; refresh for scope, freshness, contradictions, or verification. Summaries do not become authoritative through reuse. Prefer focused follow-ups unless independence or reliability needs fresh context.

Track every worker through collection or confirmed cancellation. Use supported lifecycle controls, confirm stopped operations, and inspect partial changes before retrying, transferring ownership, or finalizing affected artifacts. Incorporate user steering into active contracts. Never leave an uncollected worker changing a final deliverable.

When inputs, requirements, or assumptions change, mark dependent outputs stale, reopen affected criteria as unverified/blocked, and update active workers. Refresh only affected work, preserve unaffected results, and check derived artifacts against current inputs before finalization.

## Reassess effort and recover

For extended work, identify the next meaningful checkpoint: collection, integration, or focused recovery. Reassess before material expansion, after significant replanning, and near explicit user/runtime limits. Assess evidence gained, remaining criteria, applicable limits/observable effort, and the gap the next action would resolve. Continue, correct, replan, or finish directly using the delegation cost-benefit test; briefly explain material changes.

Checkpoints are internal decisions, not routine approval pauses or reasons to abandon unfinished work. Preserve scope, acceptance, and required checks. Respect hard limits and report unresolved criteria if they prevent completion; continue useful unaffected work where feasible.

For failure, assess cause, dependencies, ownership, and verified partial results. Keep dependents blocked. Supply missing context, use an available source/tool alternative, narrow/split assignments, serialize interference, request targeted evidence, or complete directly. Stop a failed branch with alternatives when recovery is infeasible. Retry only with a plausible changed condition; never repeat unchanged failure. Update contracts/graph and recheck recovered outputs without duplicating side effects.

Notify the user when failure materially affects quality, timing, scope, or deliverables, stating impact and revised approach/trade-offs. Routine authorized recovery proceeds directly. Seek a decision only for new authorization or consequential unaccepted trade-offs; otherwise report precise blockers, completed work, and alternatives.

## Integrate, verify, and finish

The root owns framing, evidence weighting, conflict resolution, integration, and judgment. Distinguish facts, assumptions, and inferences; resolve disagreement with evidence/follow-up rather than voting. Deliver a coherent result, not concatenated reports.

Use a separate verifier when the particular claim's consequences, uncertainty, or integration risk warrant it; domain significance alone does not justify reviewing every minor edit. Give original requirements and relevant primary evidence/artifacts without seeding the conclusion. Self-checks alone cannot satisfy required independent verification.

Choose checks suited to the claim through specialist methods. Fresh agents can share mistaken assumptions: seek independent evidence/methods where material, such as primary-source inspection, recalculation, counterexamples, rendering, or behavioral tests. Agent agreement alone is not verification. Inspect integration where it can introduce errors; fix material findings and recheck affected work. Distinguish self-checks from unavailable independent checks. Reuse primary evidence for separate assessment; do not repeat passed checks without a material reason or expand review without the cost-benefit test.

Before claiming completion, collect all dispatched outputs or confirm cancelled workers have stopped; inspect partial changes, satisfy dependencies/checks, and reconcile findings and required criteria against the current integrated result. Stop when completion evidence is satisfied. Report results, verification, limitations, and material unmet/blocked/unverified criteria. Distinguish success from hard-limit or blocker stops; blocked prerequisites cannot become success claims.

## Design reference

For maintenance, consult [design-sources.md](references/design-sources.md). Routine use requires neither loading nor installing those references.
