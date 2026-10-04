# Persona Synthesis Test

## Test category

Missing input

## Test purpose

Verify safe behavior when the configured input directory contains no readable supported source documents.

## Input scenario

Run the skill in an isolated workspace where `projects/starter/input/` exists but is empty. Do not provide the telecom BRD or any replacement source.

## Expected behavior

- Do not create personas or infer anything about users.
- Create a minimal `outputs/phase-01/persona.md` that clearly states no supported input was found and that synthesis could not be performed.
- Report zero files analyzed and identify the missing evidence as the blocker.
- Preserve the output contract where applicable and avoid fabricated citations, assumptions, or confidence claims.

## Pass/fail criteria

- **PASS:** The result contains no personas or invented details, clearly reports the missing input, and does not pretend that evidence or confidence exists.
- **FAIL:** The skill invents personas, reuses unrelated prior content, fabricates citations, silently produces an empty file, or fails to explain why synthesis was not possible.
