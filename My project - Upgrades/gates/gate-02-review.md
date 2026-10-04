---
gate: D2
name: Human Ideation Review
type: human-in-the-loop
phase_workflow: workflow/run-phase-02.md
research_evidence:
  - outputs/phase-01/persona.md
  - outputs/phase-01/pain-points.md
  - outputs/phase-01/secondary-research-report.md
artefacts:
  - outputs/phase-02/feature-opportunities.md
  - outputs/phase-02/concept-direction.md
decision_record: outputs/reviews/d2-review.md
approve_to: design or build work
---

# Gate D2 — Human Ideation Review

D2 is the mandatory human approval gate between Phase 2 ideation and subsequent design or build work. No downstream work may treat the Phase 2 artefacts as an approved brief until a human reviewer explicitly records `APPROVE`.

The product ideation agent may create or revise the artefacts and summarize evidence for review, but it must never approve D2, record a decision on the reviewer's behalf, or advance the workflow. Silence, automated validation, agent validation, or a request to continue is not approval.

## Review access and order

The reviewer may inspect the D1-approved Phase 1 evidence at any point:

1. `outputs/phase-01/persona.md`
2. `outputs/phase-01/pain-points.md`
3. `outputs/phase-01/secondary-research-report.md`

Review the required Phase 2 artefacts in this order:

1. `outputs/phase-02/feature-opportunities.md`
2. `outputs/phase-02/concept-direction.md`

Do not review the concept independently of the feature list or review the feature list independently of its Phase 1 evidence. Project-specific persona and pain evidence must remain distinguishable from market statistics, standards, competitor documentation, company claims, and anecdotal community signals.

## Review 1 — Feature opportunities

Confirm that:

- the document contains 3–7 consolidated, outcome-focused opportunities;
- every opportunity states its user outcome, precise research trace, `Critical`, `Important`, or `Helpful` priority, capability description, observable success signals, and assumptions or validation needs;
- every opportunity is supported by a persona goal or pain theme, and secondary research is used only as qualified context or corroboration;
- external claims preserve source links and geographic, methodological, access, and generalisability limitations;
- priorities reflect user impact and evidence strength rather than implementation effort;
- every Critical pain theme is covered by a Critical or Important opportunity or visibly flagged as unresolved;
- overlapping opportunities have been consolidated and unsupported ideas are excluded or explicitly labeled as assumptions;
- the coverage check and Gaps section accurately expose weak evidence, transferability concerns, unsupported groups, and open questions; and
- no opportunity is presented as a committed solution, confirmed requirement, technical specification, estimate, or delivery commitment.

## Review 2 — Concept direction

Confirm that:

- the concept identifies one primary persona and one meaningful user outcome;
- it uses the smallest necessary set of traceable Critical and Important opportunities;
- selected opportunities exist in `outputs/phase-02/feature-opportunities.md` and preserve their names, priorities, and research traces;
- the core journey connects the starting situation, user action, system response, and successful outcome coherently;
- key experience moments describe their purpose and research trace rather than visual styling;
- included scope, excluded scope and reasons, assumptions, validation questions, and design handoff are explicit;
- citations, external links, confidence and evidence limits, contradictions, gaps, and open questions are carried forward;
- Helpful or weakly supported ideas are excluded from the focused concept unless their inclusion is explicitly justified;
- an addition absent from the opportunity list is labeled as an assumption requiring validation; and
- the concept is a testable direction, not a final interface, technical architecture, implementation plan, estimate, requirement set, or delivery commitment.

## Human decision

The reviewer must choose exactly one decision:

| Decision | Meaning | Required action |
|---|---|---|
| `APPROVE` | D2 is cleared. | Release `outputs/phase-02/feature-opportunities.md` and `outputs/phase-02/concept-direction.md` to the next design or build activity with all limitations and validation needs preserved. |
| `REVISE` | One or both Phase 2 artefacts need correction within the approved evidence base. | Provide actionable feedback naming the affected artefact, evidence or scope issue, and acceptance condition. Rerun only the affected ideation step and its downstream dependency, then return to D2. |
| `REQUEST_MORE_RESEARCH` | A responsible ideation decision requires new or revised Phase 1 evidence. | Stop Phase 2, return the affected question to `workflow/run-phase-01.md`, rerun required research dependencies, obtain renewed D1 approval, then regenerate affected Phase 2 artefacts and return to D2. |

The future human decision, feedback, and disposition must be recorded in `outputs/reviews/d2-review.md`. Do not infer or create that record before a human makes a decision.

## Revision dependency logic

- If `outputs/phase-02/feature-opportunities.md` changes, validate it and regenerate `outputs/phase-02/concept-direction.md` before returning both artefacts to D2.
- If only `outputs/phase-02/concept-direction.md` changes, rerun only concept synthesis and its validation; keep the validated feature list unchanged.
- If any Phase 1 artefact changes, invalidate the affected Phase 2 outputs, rerun the required Phase 1 dependencies, obtain renewed D1 approval, then rerun feature decomposition followed by concept direction.
- If a reviewer requests more research, preserve the exact open question and affected decision when returning to Phase 1.
- If no artefact changes, D2 remains pending until an explicit human decision is recorded.

## Gate outcome

- Only explicit human `APPROVE` clears D2 and permits design or build handoff.
- `REVISE` returns work only to the affected Phase 2 step and required downstream dependency; it does not clear D2.
- `REQUEST_MORE_RESEARCH` stops Phase 2 and returns the affected issue through Phase 1 and D1; it does not clear D2.
- Approval does not turn hypotheses into validated user needs, confirmed requirements, final designs, technical commitments, or delivery commitments.
- The receiving team must preserve citations, confidence labels, evidence strengths, source links, assumptions, contradictions, geographic and methodological limitations, research gaps, scope exclusions, and validation questions.
