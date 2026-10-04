# Persona Synthesis Test

## Test category

Edge case

## Test purpose

Verify that the skill handles overlapping target-user definitions and limited single-source evidence without forcing artificial segmentation.

## Input scenario

Use `projects/starter/input/telecom-device-upgrade-existing-line-brd.md`, but evaluate the target groups as overlapping needs rather than mutually exclusive demographics. An existing postpaid customer may also be budget-conscious and may also need device guidance. No participant-level research is available to prove stable segments or prevalence.

## Expected behavior

- Recognize and disclose that the three BRD target groups may overlap.
- Create only defensible need-based personas or provisional modes; combine groups if the evidence cannot support meaningful separation.
- Avoid claiming that the groups are mutually exclusive or representative of most users.
- Record the single-source and missing-research limitations.
- Keep facts, inferences, assumptions, and any contradictions separate with confidence labels and citations.

## Pass/fail criteria

- **PASS:** The output avoids artificial differences, explains overlap and evidence limits, retains the required persona fields, cites the BRD, and labels every insight appropriately.
- **FAIL:** The output fabricates distinguishing details, implies unsupported prevalence, forces three unsupported personas, omits confidence levels, or hides the overlap limitation.
