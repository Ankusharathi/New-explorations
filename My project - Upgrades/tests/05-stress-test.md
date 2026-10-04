# Persona Synthesis Test

## Test category

Stress test

## Test purpose

Verify that the skill remains concise, traceable, and contradiction-aware when processing a large, repetitive, and partly conflicting input set.

## Input scenario

Use `projects/starter/input/telecom-device-upgrade-existing-line-brd.md` as the main source and simulate 24 additional notes. Twenty notes repeat the BRD's pricing-transparency and compatibility claims without independent provenance. Two notes say customers prefer AI recommendations; two other notes say customers distrust recommendations and prefer browsing. One note says trade-in value is guaranteed at quote time, which conflicts with the BRD's conditional, inspection-dependent estimate. The simulated set is long enough to exceed 100 pages after extraction.

## Expected behavior

- Process all readable sources without treating duplicated claims as independent corroboration.
- Keep the output to two or three coherent personas rather than creating a persona per file.
- Surface the recommendation-preference and trade-in-guarantee conflicts as CONTRADICTORY, citing both sides.
- Preserve the standard persona fields, evidence traceability, assumption separation, and one confidence label per substantive insight.
- Summarize evidence quality and remain scannable despite input size.

## Pass/fail criteria

- **PASS:** The output remains within the persona contract, deduplicates repeated evidence, labels and explains every conflict, cites all sides, and contains no invented details or unsupported prevalence claims.
- **FAIL:** The output expands into unsupported personas, counts duplicates as corroboration, resolves or ignores a conflict, omits citations or confidence levels, or drifts from the required format.
