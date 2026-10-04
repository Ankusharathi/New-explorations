---
name: feature-decomposition-skill
description: Turn approved personas, pain points, and secondary research into a prioritised, research-traceable feature opportunity list in outputs/phase-02/feature-opportunities.md.
---

# Name & Description

**Feature Decomposition Skill**

Translate approved research into a concise set of feature opportunities. Each opportunity must solve a persona-supported problem or help a persona reach a stated goal.

# Role

Act as a product-thinking partner. Convert user pain points into clear, testable opportunities while preserving evidence links, uncertainty, and scope discipline.

# Instructions

1. Read `outputs/phase-01/persona.md`, `outputs/phase-01/pain-points.md`, and `outputs/phase-01/secondary-research-report.md` in full.
2. Extract the highest-impact persona goals, pain themes, design opportunities, evidence strengths, relevant external findings, and open validation questions. Keep primary project evidence, secondary evidence, and synthesis distinguishable.
3. Create 3–7 feature opportunities. Consolidate overlapping ideas rather than creating duplicates.
4. For each opportunity, define:
   - the user outcome;
   - the research trace;
   - priority based on user impact and evidence strength;
   - a short description of the capability;
   - testable success signals;
   - assumptions, dependencies, or validation needs.
5. Label priorities as `Critical`, `Important`, or `Helpful`.
6. Check coverage: each critical pain theme should be served by at least one critical or important opportunity. Flag any uncovered theme.
7. Create `outputs/phase-02/` if it does not exist and write the final document to `outputs/phase-02/feature-opportunities.md`.
8. Review the document before completion. Confirm that no feature is based only on a preferred interface pattern or unsupported assumption.

# Input

Read these approved Phase 1 outputs:

```text
outputs/phase-01/persona.md
outputs/phase-01/pain-points.md
outputs/phase-01/secondary-research-report.md
```

If any file is missing, stop and report which Phase 1 output is required.

# Output

Write one Markdown file to:

```text
outputs/phase-02/feature-opportunities.md
```

Use this output structure:

```markdown
# Feature Opportunities

## Research Basis

- Personas used: [persona names]
- Pain-point source: `outputs/phase-01/pain-points.md`
- Secondary-research source: `outputs/phase-01/secondary-research-report.md`
- Evidence limitations: [carried forward from Phase 1]

## Feature 1: [Name]

**Priority**: Critical | Important | Helpful

**User outcome**: [what the user can achieve]

**Research trace**:
- [persona goal or pain point with source locator]

**Description**:
- [capability and why it matters]

**Success signals**:
- [observable user or product outcome]

**Assumptions and validation needs**:
- [what must be tested]

## Coverage Check

| Pain theme | Feature opportunity | Coverage status |
|------------|---------------------|-----------------|
| [theme] | [feature] | Covered | Needs decision |

## Gaps

- [uncovered pain, weak evidence, or research needed]
```

# Rules & Guardrails

- Use only the three Phase 1 outputs listed above as research evidence.
- Keep project-specific persona and pain-point evidence distinct from external secondary evidence. Do not treat market statistics, competitor documentation, standards, or anecdotal community posts as direct evidence of the project's users.
- Preserve links and source descriptions for every external claim used. Carry forward geographic, methodological, and generalisability limitations.
- Do not invent user needs, pain points, capabilities, or requirements.
- A feature opportunity is a hypothesis; never present it as a committed solution.
- Preserve the evidence limitations, assumptions, and open questions from Phase 1.
- Prioritise by user impact and evidence strength, not implementation effort.
- Keep features outcome-focused. Avoid naming a UI element as the feature unless the research establishes that specific solution.
- Do not modify Phase 1 outputs.
- Write only the final opportunity list to `outputs/phase-02/feature-opportunities.md`.

# Example

If a pain theme says users cannot understand monthly spending without manual tracking, an acceptable opportunity is:

```markdown
## Feature 1: Automatic spending overview

**Priority**: Critical

**User outcome**: Users can understand their monthly spending without recording every transaction themselves.

**Research trace**:
- Manual tracking feels burdensome — `[outputs/phase-01/pain-points.md, Delayed visibility into spending]`

**Description**:
- Present an automatically assembled spending overview with clear category totals.

**Success signals**:
- Users can identify their highest spending category without manual entry.

**Assumptions and validation needs**:
- Test whether users trust the automatic categorisation enough to rely on the overview.
```
