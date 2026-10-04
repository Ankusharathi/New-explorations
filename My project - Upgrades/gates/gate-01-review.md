---
gate: D1
name: Human Research Review
type: human-in-the-loop
phase_workflow: workflow/run-phase-01.md
source_evidence: projects/starter/input/
artefacts:
  - outputs/phase-01/persona.md
  - outputs/phase-01/pain-points.md
  - outputs/phase-01/secondary-research-report.md
decision_record: outputs/reviews/d1-review.md
approve_to: workflow/run-phase-02.md
---

# Gate D1 — Human Research Review

D1 is a mandatory human approval gate between Phase 1 and Phase 2. Phase 2 must not begin until a human reviewer explicitly records `APPROVE`. The researcher agent may revise research artefacts in response to feedback, but it must never approve D1 or advance the workflow to Phase 2.

Silence, agent validation, successful automated checks, or a request to continue is not approval.

## Review access and order

The human reviewer may inspect the underlying source evidence in `projects/starter/input/` at any point. Review the required artefacts in this order:

1. `outputs/phase-01/persona.md`
2. `outputs/phase-01/pain-points.md`
3. `outputs/phase-01/secondary-research-report.md`

Do not review the pain-point analysis or secondary-research report as independently validated user research. Pain points must remain traceable to the reviewed persona synthesis, and secondary research must preserve the limitations of any local artefact it uses.

## Review 1 — Persona synthesis

Confirm that:

- citations resolve to the supplied source evidence and accurately represent the cited material;
- facts or direct source claims, synthesis, and assumptions are clearly separated;
- every assumption and validation need is explicit;
- evidence limitations, including source quality, independence, sample, recency, and representativeness, are visible and proportionate;
- contradictions are identified, cite every side, and remain unresolved rather than averaged away;
- research gaps and missing groups are recorded;
- confidence labels reflect the evidence and do not present business claims as validated user research; and
- no persona, demographic, quotation, behaviour, need, motivation, prevalence claim, or finding has been invented.

## Review 2 — Pain-point analysis

Confirm that:

- every pain theme and evidence note is traceable to `outputs/phase-01/persona.md`;
- persona assumptions, contradictions, evidence limitations, and research gaps are carried forward;
- evidence strength is accurate and is not inflated by a persona confidence label or a plausible solution;
- priorities reflect user impact and evidence strength rather than implementation effort;
- design opportunities are grounded in supported pain and use appropriate problem framing;
- likely feature directions remain hypotheses rather than confirmed requirements;
- validation questions address the most consequential uncertainty; and
- vague, unsupported, or untraceable pain themes are removed, narrowed, marked Weak, or moved to Gaps.

## Review 3 — Secondary research

Confirm that:

- every statistic and consequential claim has a traceable citation and every cited source appears in the appendix;
- source dates, geography, population or sample, method, sponsorship, recency, and access limitations are disclosed when available;
- authoritative sources are distinguished from company claims, direct product observations, journalism, sponsored evidence, reviews, forums, and researcher inference;
- competitor strengths, gaps, and patterns are based on observable or cited evidence and do not imply access to unobserved account-specific flows;
- forums, app reviews, Reddit, and Quora are treated as non-representative qualitative signals rather than prevalence evidence;
- conflicts and transfer limitations across markets, platforms, and time periods remain visible;
- recommendations follow from cited findings, and provisional directions are not presented as confirmed user needs or requirements;
- the report preserves limitations from the persona and pain-point artefacts where it relies on them; and
- unanswered questions are routed to primary research validation rather than answered through unsupported assumptions.

## Human decision

The reviewer must choose exactly one decision:

| Decision | Meaning | Required action |
|---|---|---|
| `APPROVE` | D1 is cleared. | Allow handoff to `workflow/run-phase-02.md`. Approval must be explicit and human-authored. |
| `REVISE` | One or more artefacts need correction. | Provide actionable feedback identifying the affected artefact, evidence issue, and acceptance condition. Rerun only the affected `researcher-agent` step and required downstream dependencies, then return to D1. |
| `REJECT` | Phase 1 lacks evidence adequate for responsible progression. | Stop the workflow at Phase 1 until better research evidence is available and the affected synthesis has been rerun and reviewed. |

The future human decision, reviewer feedback, and disposition should be recorded in `outputs/reviews/d1-review.md`. Do not infer or pre-create that record before a human makes a decision.

## Revision dependency logic

- If `outputs/phase-01/persona.md` changes, validate it, regenerate `outputs/phase-01/pain-points.md`, and refresh `outputs/phase-01/secondary-research-report.md` before returning all artefacts to D1.
- If only `outputs/phase-01/pain-points.md` changes, rerun pain-point extraction and then refresh the secondary-research report; keep the validated persona unchanged.
- If only `outputs/phase-01/secondary-research-report.md` changes, rerun only secondary research and its validation; keep the validated persona and pain points unchanged.
- If no artefact changes, D1 remains pending until an explicit human decision is provided.

## Gate outcome

- Only explicit human `APPROVE` clears D1 and permits Phase 2 handoff.
- `REVISE` returns work only to the affected Phase 1 step and does not clear D1.
- `REJECT` stops the workflow at Phase 1 and does not clear D1.
- The researcher agent may prepare revisions and evidence summaries, but it cannot select or record the approval decision on the human reviewer's behalf.
