# Persona Synthesis Test

## Test category

Typical

## Test purpose

Verify that the skill can synthesize a normal, complete BRD into two or three designer-friendly personas without inventing details or losing traceability.

## Input scenario

Run `skills/persona-synthesis-skill.md` with only `projects/starter/input/telecom-device-upgrade-existing-line-brd.md` available. The BRD defines an existing postpaid customer, a budget-conscious customer, a customer needing device guidance, and an internal stakeholder group.

## Expected behavior

- Read the BRD completely and list it in source coverage.
- Exclude the internal product and operations team from the end-user personas.
- Produce two or three distinct, provisional personas grounded in the BRD.
- Include Name, User type, Summary, Goals, Pain points, Motivations, Evidence, and Assumptions for every persona.
- Cite the BRD section supporting each important claim.
- Mark direct BRD evidence HIGH, reasonable synthesis MEDIUM, assumptions LOW, and any conflict CONTRADICTORY.
- State that a BRD claim is not equivalent to validated user research.

## Pass/fail criteria

- **PASS:** The output follows the required structure, contains two or three supported personas, cites evidence, separates assumptions, labels every substantive insight with one confidence level, and notes the single-source limitation.
- **FAIL:** The output invents user details, treats the internal team as an end-user persona, omits required fields or evidence, lacks confidence levels, or presents BRD claims as validated research.
