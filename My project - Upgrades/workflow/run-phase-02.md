---
phase: 2
name: Ideate
entry_from: workflow/run-phase-01.md
trigger: Phase 1 persona, pain-point, and secondary-research outputs have current explicit human D1 approval
gate: gates/gate-02-review.md
team:
  lead: agents/product-ideation-agent.md
agents:
  - agents/product-ideation-agent.md
skills_invoked:
  - skills/feature-decomposition-skill.md
  - skills/concept-direction-skill.md
inputs:
  - outputs/phase-01/persona.md
  - outputs/phase-01/pain-points.md
  - outputs/phase-01/secondary-research-report.md
  - outputs/reviews/d1-review.md
outputs:
  - outputs/phase-02/feature-opportunities.md
  - outputs/phase-02/concept-direction.md
exports:
  - outputs/phase-02/feature-opportunities.md
  - outputs/phase-02/concept-direction.md
exit_to: design or build work
---

# P2 — Ideate

Turn the D1-approved Phase 1 research package into a small set of traceable feature hypotheses and one focused concept direction. Phase 2 must preserve project-user evidence separately from external context and must not convert hypotheses into confirmed requirements or delivery commitments.

## Agent Team

| Role | Agent | Produces |
|---|---|---|
| Lead | `agents/product-ideation-agent.md` | `outputs/phase-02/feature-opportunities.md`; `outputs/phase-02/concept-direction.md`; unresolved gaps, trade-offs, assumptions, and validation needs |

## Execution Sequence

| Step | Who | Skills | Input | Output | Gate |
|---:|---|---|---|---|---|
| 1 | `agents/product-ideation-agent.md` | — | Agent definition, both skill files, all three Phase 1 artefacts, and `outputs/reviews/d1-review.md` | Readiness assessment and confirmed current D1 approval | Research handoff ready |
| 2 | `agents/product-ideation-agent.md` | `skills/feature-decomposition-skill.md` | `outputs/phase-01/persona.md`, `outputs/phase-01/pain-points.md`, `outputs/phase-01/secondary-research-report.md` | `outputs/phase-02/feature-opportunities.md` | Feature opportunities valid |
| 3 | `agents/product-ideation-agent.md` | `skills/concept-direction-skill.md` | All three Phase 1 artefacts and validated `outputs/phase-02/feature-opportunities.md` | `outputs/phase-02/concept-direction.md` | Concept direction valid |
| 4 | Human reviewer | — | Both validated Phase 2 outputs and their research traces | Explicit D2 approval, actionable revision request, or request for more research | D2 |

**Order is mandatory:** Step 3 must not begin until Step 2 passes validation. Phase 2 must not begin until all three Phase 1 artefacts are current and `outputs/reviews/d1-review.md` records explicit human `APPROVE` covering them.

For an end-to-end request beginning with the BRD or `projects/starter/input/`, `agents/product-ideation-agent.md` must invoke `agents/researcher-agent.md` before this phase. The researcher agent may validate and skip unchanged Phase 1 steps, but changed research must run through persona synthesis → pain-point extraction → secondary research and return to D1 before Phase 2 starts.

## Phase Inputs and Read Rules

Before creating or replacing a Phase 2 artefact, read in full:

1. `agents/product-ideation-agent.md` — ownership, upstream research dependency, decision rules, handoff, completion format, and recovery actions.
2. `skills/feature-decomposition-skill.md` — feature-opportunity inputs, evidence rules, output contract, coverage check, and validation requirements.
3. `skills/concept-direction-skill.md` — concept inputs, mandatory dependency on feature opportunities, output contract, scope rules, and validation requirements.
4. `outputs/phase-01/persona.md` — persona goals, pain points, confidence labels, citations, assumptions, contradictions, limitations, and open questions.
5. `outputs/phase-01/pain-points.md` — pain themes, evidence strength, design opportunities, priorities, gaps, and validation needs.
6. `outputs/phase-01/secondary-research-report.md` — cited market, standards, competitor, and behavioural context with geographic, methodological, access, and generalisability limits.
7. `outputs/reviews/d1-review.md` — the explicit human D1 decision and the exact Phase 1 artefacts approved.

### Evidence Rules

1. Use `persona.md` and `pain-points.md` as the source of truth for project-user problems and goals.
2. Use secondary research only to contextualise or corroborate. Keep market statistics, standards, competitor documentation, company claims, and anecdotal community signals distinct from direct project-user evidence.
3. Preserve a precise research trace for every feature opportunity and key concept decision. Preserve external links and source descriptions when external evidence is used.
4. Carry forward confidence labels, evidence strengths, assumptions, contradictions, weak evidence, research gaps, access limits, geographic limits, and open validation questions.
5. Do not upgrade LOW, Weak, inferred, anecdotal, provisional, or market-specific evidence because an idea appears useful.
6. Do not introduce features because they are fashionable, technically convenient, common among competitors, or visually appealing without project research support.
7. Treat every opportunity and concept direction as a hypothesis until validated. Do not present it as a confirmed requirement, technical plan, estimate, or delivery commitment.
8. If the Phase 1 handoff is missing, stale, inconsistent, unreadable, or inadequately approved, stop and return only the affected work to `workflow/run-phase-01.md`.

## Part A — Feature Decomposition

- **Agent:** `agents/product-ideation-agent.md`
- **Skill:** `skills/feature-decomposition-skill.md`
- **Input:** `outputs/phase-01/persona.md`, `outputs/phase-01/pain-points.md`, `outputs/phase-01/secondary-research-report.md`
- **Output:** `outputs/phase-02/feature-opportunities.md`

### Step A1 — Research handoff check

Read all three Phase 1 artefacts and the D1 review in full. Confirm that the persona contains cited goals or pain points; the pain-point analysis contains traceable themes, evidence strengths, priorities, opportunities, and gaps; secondary research contains traceable citations and limitations; and D1 records explicit human `APPROVE` for the current versions.

**Block condition:** If a Phase 1 artefact or current D1 approval is missing, incomplete, stale, inconsistent, or unreadable, stop Phase 2. Return the affected work to `agents/researcher-agent.md` and require renewed D1 approval after any Phase 1 change. Do not infer approval or create opportunities from an unsupported handoff.

### Step A2 — Create feature opportunities

Translate the highest-impact persona goals and pain themes into 3–7 consolidated, outcome-focused opportunities. For each opportunity include:

- user outcome;
- precise research trace;
- `Critical`, `Important`, or `Helpful` priority based on user impact and evidence strength rather than implementation effort;
- a short capability description;
- observable success signals; and
- assumptions, dependencies, or validation needs.

Keep project evidence distinguishable from secondary context. Preserve links and limitations for external claims. Cover every Critical pain theme with at least one Critical or Important opportunity or flag it as uncovered.

### Step A3 — Feature opportunity validation

- [ ] `outputs/phase-02/feature-opportunities.md` exists and contains 3–7 consolidated opportunities.
- [ ] Every opportunity includes a user outcome, research trace, valid priority, capability description, success signals, and validation needs.
- [ ] Every opportunity links to at least one persona-supported goal or pain point.
- [ ] Priority reflects user impact and evidence strength, not implementation effort.
- [ ] Opportunities describe outcomes rather than only interface elements.
- [ ] Project-user evidence and external secondary evidence remain distinguishable.
- [ ] External claims preserve source links and geographic, methodological, access, and generalisability limits.
- [ ] Every Critical pain theme is covered by a Critical or Important opportunity or visibly flagged as uncovered.
- [ ] Overlapping ideas are consolidated; unsupported ideas are excluded or explicitly labeled as assumptions.
- [ ] No opportunity is presented as a committed solution or confirmed requirement.

If any check fails, revise `outputs/phase-02/feature-opportunities.md` and repeat validation before continuing. If a Critical pain theme remains uncovered and the correct scope is unclear, stop for a human decision before Part B.

## Part B — Concept Direction

- **Agent:** `agents/product-ideation-agent.md`
- **Skill:** `skills/concept-direction-skill.md`
- **Input:** All three approved Phase 1 outputs and validated `outputs/phase-02/feature-opportunities.md`
- **Output:** `outputs/phase-02/concept-direction.md`

### Step B1 — Select a focused direction

Identify one primary persona, one meaningful user outcome, and the smallest necessary set of traceable Critical and Important opportunities. Leave Helpful or weakly supported opportunities outside the initial concept unless evidence justifies inclusion.

**Block condition:** If `outputs/phase-02/feature-opportunities.md` is missing, fails validation, or contains a selected opportunity without a research trace, return to Part A. Concept direction cannot precede or bypass feature decomposition.

### Step B2 — Create concept direction

Describe one core journey from the user's starting situation to a successful outcome. Include the research basis, concept statement, four-step core journey, key experience moments and their purpose, included scope, excluded scope and reasons, assumptions, validation questions, and design handoff.

Do not add an opportunity absent from the feature list unless it is necessary to explain the concept and is explicitly labeled as an assumption requiring validation. Do not specify visual styling, components, technical architecture, implementation details, estimates, or delivery commitments.

### Step B3 — Concept direction validation

- [ ] `outputs/phase-02/concept-direction.md` exists.
- [ ] The concept focuses on one primary persona and one meaningful outcome.
- [ ] It uses the smallest necessary set of traceable Critical and Important opportunities.
- [ ] The core journey connects selected opportunities into one coherent experience.
- [ ] Key moments describe purpose rather than visual styling.
- [ ] Included and excluded scope are clearly separated.
- [ ] Assumptions and validation questions are visible.
- [ ] Citations, external links, evidence limitations, contradictions, gaps, and open questions are carried forward.
- [ ] Any addition absent from the feature list is explicitly labeled as an assumption.
- [ ] The document contains no technical plan, estimate, delivery commitment, or claim that a hypothesis is confirmed.

If the concept is too broad, reduce it to one outcome and the smallest necessary opportunity set. If evidence is contradictory, weak, stale, or market-specific in a way that materially changes the concept, preserve the limitation and stop for human direction.

## D2 Gate — Ideation Approval

D2 is governed by [Gate D2 — Human Ideation Review](../gates/gate-02-review.md). The product ideation agent may create or revise artefacts but cannot approve D2, record a decision for the reviewer, or infer approval from silence, automated validation, agent validation, or a request to continue.

### Required artefacts

| # | Path | Author | Required checks |
|---:|---|---|---|
| 1 | `outputs/phase-02/feature-opportunities.md` | `agents/product-ideation-agent.md` using `skills/feature-decomposition-skill.md` | Research traces, outcomes, priorities, capability descriptions, success signals, coverage check, assumptions, limitations, and gaps |
| 2 | `outputs/phase-02/concept-direction.md` | `agents/product-ideation-agent.md` using `skills/concept-direction-skill.md` | Primary persona and outcome, core journey, key moments, scope boundaries, research traces, assumptions, limitations, and validation questions |

### Approval checklist

- [ ] Every selected feature opportunity is supported by Phase 1 project evidence; secondary research is used only as qualified context or corroboration.
- [ ] Critical pain themes are covered or explicitly recorded as unresolved.
- [ ] Priorities reflect user impact and evidence strength rather than implementation effort.
- [ ] The concept is small enough to communicate one primary user outcome.
- [ ] Included and excluded scope, assumptions, evidence limits, contradictions, and open questions are explicit.
- [ ] Feature opportunities and concept direction remain hypotheses rather than confirmed requirements or delivery commitments.
- [ ] A Human reviewer explicitly approves the outputs for design or build work.

The reviewer may:

- **APPROVE:** clear D2 and release the two exports to the next design or build activity;
- **REVISE:** provide actionable feedback and rerun only the affected ideation step plus any dependent downstream step; or
- **REQUEST MORE RESEARCH:** return the affected question to Phase 1, rerun the required research dependencies, obtain renewed D1 approval, and then rerun affected Phase 2 work.

Do not advance until D2 receives explicit human approval. The future decision must be recorded in `outputs/reviews/d2-review.md`; do not create or infer that record before the human review. If feature opportunities change, revalidate them and regenerate concept direction before returning to D2. If only concept direction changes, rerun only concept synthesis and its validation.

## Exceptions

| Condition | Action |
|---|---|
| A Phase 1 output is missing, unreadable, incomplete, stale, or unapproved | Stop and return the affected work to `agents/researcher-agent.md`; require renewed D1 approval after any change. |
| Secondary research is missing or unverifiable | Stop before feature decomposition; remove or qualify unsupported claims and restore citations through the researcher agent. |
| External evidence is presented as direct project-user evidence | Separate the evidence types, restore source links and limitations, and revise the affected opportunity or concept claim. |
| A feature has no research trace | Exclude it; if necessary to describe unresolved direction, label it as an assumption with a validation question. |
| Feature opportunities overlap | Consolidate them and preserve the shared evidence links, limitations, and validation needs. |
| A Critical pain theme is uncovered | Add a supported Critical or Important opportunity, or flag the gap and request a human scope decision before concept synthesis. |
| Feature priority is unsupported | Reassess using user impact and evidence strength; if still uncertain, mark it provisional and add a validation question. |
| Feature opportunities conflict | Preserve the trade-off and evidence on each side; do not resolve it silently. Request a reviewer decision when it materially changes scope. |
| The concept is too broad | Reduce it to one primary persona, one outcome, and the smallest necessary Critical and Important opportunity set. |
| The concept references an absent or untraceable feature | Return to Part A, correct and validate the opportunity list, then regenerate concept direction. |
| Evidence is contradictory, weak, stale, or market-specific | Preserve the limitation, do not raise certainty, add a validation question, and stop for human direction when material. |
| A Phase 1 artefact changes after Phase 2 synthesis | Invalidate affected Phase 2 outputs; rerun required Phase 1 dependencies and D1, then feature decomposition followed by concept direction. |
| An output cannot be written safely | Stop and report the exact path or conflict; do not write elsewhere or overwrite a conflicting validated file silently. |

## Phase Handoff

After explicit human D2 approval, export:

- `outputs/phase-02/feature-opportunities.md`
- `outputs/phase-02/concept-direction.md`

The receiving design or build team must preserve citations, confidence labels, evidence strengths, external links, assumptions, contradictions, geographic and methodological limitations, research gaps, scope exclusions, and open validation questions. It must use the artefacts as a decision-making brief and must not treat feature opportunities, likely feature directions, design opportunities, or the concept direction as confirmed requirements, final interface specifications, technical commitments, or delivery commitments.
