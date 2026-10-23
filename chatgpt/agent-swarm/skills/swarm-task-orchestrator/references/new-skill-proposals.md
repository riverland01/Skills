# From a solved problem to a new problem-specific skill

`proposed_new_skills` replaces orchestrator-update/patch proposals. The target is a separate problem-family skill; orchestrator maintenance requires its own user request.

## Candidate gate

Require a checked reusable method, plausible recurrence, meaningful value beyond accessible existing skills, and supported boundaries. Check overlap proportionately; disclose uninspected coverage rather than claim uniqueness. Unverified results remain notes/hypotheses. A verified subworkflow supports only its demonstrated scope; one successful case proves no generality. Most decompositions remain run records.

Extract successful dependencies, decisions, alternatives, checks, assumptions, limits, and capability requirements. Parameterize incidental names, values, dates, paths, order, and failures. Do not automatically inherit a fixed roster or the full orchestrator.

## Proposal record

Adapt without empty-field boilerplate:

```yaml
proposed_new_skills:
  - name: "distinct-lowercase-problem-family"
    purpose: "Recurring problem"
    trigger: "Activating requests"
    applicability: []
    exclusions: []
    required_inputs: []
    outputs_and_acceptance: []
    reusable_workflow:
      - step: "Parameterized action/decision"
        prerequisites: []
        evidence_or_exit_check: "What establishes the result"
    decision_rules_and_alternatives: []
    capability_requirements_and_fallbacks: []
    demonstrated_scope: "Checked run/subworkflow"
    run_evidence_locations: []
    material_assumptions_and_limits: []
    existing_skill_overlap: "Known overlap or not checked"
    validation_plan:
      distinct_case: "Different instance"
      boundary_case: "Adapt, decline, or expose a gap"
      required_observations: []
    maturity: proposal # proposal | draft | validated-for-stated-cases
    optional_draft_location: "Only if created"
```

Use concise provenance and accessible prerequisite references. Keep private evidence authorized; shareable drafts need checked sanitization, safe examples, and no credentials, personal data, traces, or inaccessible private paths. Do not claim checks not performed.

## Draft and validate

Default to a candidate and validation plan. If useful within allowance, draft a separate folder with valid `SKILL.md` name/description frontmatter, focused trigger, parameterized procedure, inputs, outputs, checks, and recovery. Add scripts/references only for a concrete purpose. Already authorized creation proceeds without reasking; drafts remain task artifacts unless installation is authorized. Never silently install, enable, publish, or modify either skill as a task-solving side effect.

Check format, reference accessibility, behavior on a distinct instance, and a boundary/counterexample; use independent evaluation when consequences/complexity justify it. Missing checks retain proposal/draft maturity. Source-case or format success alone proves no broad effectiveness; validation claims cover only tested cases.

The requested deliverable/checks take priority and share the hard allowance. When exhausted, preserve a brief candidate note if possible; commission no extra learning work.

## Example

A checked authorization implementation may yield `deliver-authorization-feature`: inspect identity models, conditionally plan schema/migration/rollback, implement rules, update fixtures, test allowed/denied actions, and document. Parameterize framework details; test another identity model and a policy-only change needing no migration. This creates a separate specialist proposal rather than adding a default migration agent to the orchestrator.
