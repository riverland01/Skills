# Compact coordination records

Use prose for simple assignments; adapt these fields only when useful. Maintain one authoritative record without mandatory empty-field boilerplate.

## Task and evidence record

```yaml
goal: "Requested outcome"
tasks:
  - id: T1
    objective: "Bounded output"
    depends_on: []
    required_inputs: []
    owner: coordinator
    owned_resources: []
    permitted_changes: []
    expected_output: "Artifact or supported finding"
    acceptance_ids: [C1]
    exit_requirements: []
    state: pending # pending | running | completed | blocked | failed | cancelled
    accepted_prerequisite_output: false
criteria:
  - id: C1
    requirement: "Observable outcome"
    responsible_tasks: [T1]
    status: unverified # unverified | met | unmet | blocked
    evidence: [{location: "Usable pointer", version: "When material", check_and_result: "What it establishes"}]
    unresolved_gap: "If any"
resource_ownership: []
active_workers: []
```

Only coordinator inspection sets prerequisite acceptance; completed status does not. Release dependents after all relevant exit checks pass. Final integrated artifacts may need different checks. Preserve prior evidence provenance when reopening, date sensitive sources, and record material revisions.

## Worker return extensions

All returns: status, criterion-linked findings/changes, usable evidence pointers, check results, and material gaps. Add relevant details:

- Research: inspected primary/contradictory sources, coverage, unsupported claims, citation locations.
- Analysis: input versions, assumptions, reproducible method/results, sensitivity/uncertainty.
- Editing: resources inspected/changed, produced artifacts, validation/render results, issues.
- Review: finding location/evidence, severity/impact, required versus optional fixes, unchecked scope.

"No findings" must disclose material coverage limits; precise pointers usually replace raw logs/dumps.

## Checkpoint and final run summary

```yaml
checkpoint:
  trigger: "Milestone or approaching limit"
  evidence_gained: []
  open_criteria: []
  effort_and_limits:
    hard_limits: [] # include user/runtime source
    observable_usage: "Known or unknown"
    next_soft_checkpoint: "Useful milestone"
  decision: "Continue, correct, replan, or finish directly"
  next_action_and_gap: "Action and gap addressed"
  rationale: "When material"
final:
  status: partial # complete | partial | blocked
  stopping_reason: "Acceptance, hard limit, or blocker"
  integrated_artifacts: []
  checks_and_results: []
  unresolved_criteria: []
  material_decomposition_changes: []
  rejected_findings_and_reasons: []
  workers_collected_or_confirmed_stopped: []
  proposed_new_skills: []
```

Record what actually worked; never invent usage or lessons to fill fields. Show only decision-relevant results and limits to the user.
