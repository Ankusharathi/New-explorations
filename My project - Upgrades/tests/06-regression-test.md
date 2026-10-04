# Persona Synthesis Test

## Test category

Regression test

## Test purpose

Protect previously established behavior for the telecom BRD, especially evidence labeling, required persona fields, output location, and the distinction between business claims and validated research.

## Input scenario

Run the current `skills/persona-synthesis-skill.md` against `projects/starter/input/telecom-device-upgrade-existing-line-brd.md`. Compare the behavior with the accepted baseline: three provisional need-based personas covering continuity and eligibility, price certainty, and device-selection guidance; BRD section citations; explicit source limitations; confidence labels; and a confidence/evidence review.

## Expected behavior

- Write only `outputs/phase-01/persona.md` for the persona deliverable.
- Preserve three defensible need-based personas unless new evidence justifies a different count.
- Include all eight persona fields in the documented order.
- Cite the telecom BRD precisely, distinguish business claims from research, and separate assumptions.
- Include HIGH, MEDIUM, LOW, and CONTRADICTORY semantics, confidence counts, evidence gaps, contradictions, hypotheses to test, and review guidance.

## Pass/fail criteria

- **PASS:** The current skill reproduces the baseline contract without hallucination, structural drift, missing evidence, unsupported assumptions, or missing confidence/review content.
- **FAIL:** Any baseline safeguard disappears, the output path or structure changes, personas become unsupported, evidence is omitted, or confidence and review requirements regress.
