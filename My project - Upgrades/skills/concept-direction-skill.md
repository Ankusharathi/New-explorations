---
name: concept-direction-skill
description: Turn Phase 1 personas, pain points, secondary research, and research-traceable feature opportunities into one focused product concept direction in outputs/phase-02/concept-direction.md.
---

# Name & Description

**Concept Direction Skill**

Create a focused product concept that connects the highest-priority feature opportunities into one understandable user journey. The concept is a testable direction, not a finished interface or delivery commitment.

# Role

Act as a product and experience design partner. Shape a coherent concept around a meaningful user outcome while keeping scope boundaries, research links, and uncertainty explicit.

# Instructions

1. Read `outputs/phase-01/persona.md`, `outputs/phase-01/pain-points.md`, `outputs/phase-01/secondary-research-report.md`, and `outputs/phase-02/feature-opportunities.md` in full.
2. Before synthesis, confirm that all four files exist and are readable. Do not start if `outputs/phase-02/feature-opportunities.md` is missing or if a selected feature lacks a research trace.
3. Identify the primary persona and the most important user outcome supported by the evidence.
4. Select the smallest set of Critical and Important opportunities needed to support that outcome. Preserve each selected opportunity's name, priority, and research trace.
5. Describe one core journey from the user's starting point to a successful outcome.
6. Define the concept's scope:
   - what is included now;
   - what is deliberately excluded and why;
   - which assumptions still need validation.
7. List the key screens, moments, or interactions that a later design activity should explore. Describe their purpose, not their visual styling.
8. Carry forward citations, evidence limitations, assumptions, contradictions, research gaps, and open validation questions relevant to the concept.
9. Create `outputs/phase-02/` if it does not exist and write the final document to `outputs/phase-02/concept-direction.md`.
10. Review the concept before completion. Confirm that it:
    - focuses on one primary user outcome;
    - uses only traceable Phase 1 evidence and listed feature opportunities;
    - keeps included and excluded scope distinct;
    - labels any necessary addition not present in the feature list as an assumption;
    - preserves uncertainty and validation needs; and
    - does not claim more certainty than the evidence supports.

# Input

Read these files:

```text
outputs/phase-01/persona.md
outputs/phase-01/pain-points.md
outputs/phase-01/secondary-research-report.md
outputs/phase-02/feature-opportunities.md
```

Do not start until `outputs/phase-02/feature-opportunities.md` exists and every selected feature has a research trace. If a required file is missing, unreadable, or internally inconsistent, stop and report the exact blocker rather than using a substitute or inventing content.

# Output

Write one Markdown file to:

```text
outputs/phase-02/concept-direction.md
```

Use this output structure:

```markdown
# Concept Direction

## Research Basis

- Primary persona: [name]
- Primary pain or goal: [research-traceable statement]
- Feature opportunities included: [feature names]
- Evidence limitations: [carried forward from Phase 1]

## Concept Statement

[One or two sentences explaining the experience and its intended user outcome.]

## Core Journey

1. [starting situation]
2. [key user action]
3. [system response]
4. [successful user outcome]

## Key Experience Moments

| Moment | Purpose | Research trace |
|---|---|---|
| [moment] | [what it helps the user do] | [persona or pain-point reference] |

## Scope

### Included

- [opportunity or capability]

### Excluded for now

- [capability and reason]

## Assumptions and Validation Questions

- [assumption or question]

## Design Handoff

- [what a designer should explore next]
```

Replace every bracketed prompt with sourced project content. Do not leave instructional placeholders in the completed concept.

# Rules & Guardrails

- Use only `outputs/phase-01/persona.md`, `outputs/phase-01/pain-points.md`, `outputs/phase-01/secondary-research-report.md`, and `outputs/phase-02/feature-opportunities.md` as inputs.
- Use secondary research to contextualise or corroborate a direction, not to invent project-user behaviour. Keep market statistics, standards, competitor documentation, and anecdotal community signals distinct from direct project evidence.
- Preserve links and the report's geographic, methodological, and generalisability limitations whenever secondary evidence shapes the concept.
- Do not introduce a feature that is absent from the feature-opportunity list unless it is necessary to explain the concept and is explicitly labeled as an assumption requiring validation.
- Keep the concept focused on one primary user outcome.
- Do not write visual styling, component specifications, technical architecture, implementation details, estimates, or delivery commitments.
- Preserve relevant evidence limitations, citations, assumptions, contradictions, research gaps, and open questions from earlier outputs.
- Do not upgrade LOW, Weak, inferred, or provisional evidence because a concept appears useful.
- Clearly separate included scope from excluded or future ideas.
- Do not modify any input file.
- Write only the final concept direction to `outputs/phase-02/concept-direction.md`.

# Example

If the primary pain is delayed visibility into spending, an acceptable concept statement is:

```markdown
## Concept Statement

Give people a calm, automatic snapshot of their current spending so they can understand what changed and choose one useful next step without maintaining a manual budget.
```

This describes an intended outcome. It does not assume a specific visual layout, dashboard pattern, or technical implementation.
