# Markdown specimen record format

## Purpose

This format is designed to remain readable and editable as ordinary Markdown while being regular enough for later import into a structured recording system.

## Version

Every record begins with YAML metadata and must contain:

- `record_format: specimen-record`
- `format_version: "0.1"`
- a unique `record_id`
- `record_status`, using `in-progress`, `complete`, or `withdrawn`

Do not change `format_version` within an existing record merely because the template has been updated. Migration should be deliberate and documented.

## Stable top-level headings

Keep these level-two headings exactly as written and in this order:

1. `Record`
2. `Collection and context`
3. `Specimen state`
4. `Examination plan`
5. `Observations`
6. `Preparations`
7. `Identification`
8. `Evidence`
9. `Provenance and revision history`

Fields that are unresolved should remain present with an explicit value such as `Not supplied`, `Not examined`, or `Uncertain`.

## Observation hierarchy

Within `Observations`, use level-three headings for structures or biological groupings, such as:

- `Overall habitus`
- `Head`
- `Wings`
- `Leaves`
- `Flowers`
- `Microscopy`

Add, remove, or reorder these structural headings to suit the organism. Within them, give each observation a stable level-four heading:

```markdown
#### OBS-001 — Body length

- Observation status: Observed
- Original observation: About 5 mm long.
- Normalised description: Estimated body length approximately 5 mm.
- Specimen state: Intact
- Method: Visual estimate without a scale.
- Individual measurements: Not measured
- Interpretation: None
- Supporting evidence: None
- Uncertainty or limitation: Visual estimate only.
```

Observation identifiers must be unique within the record and must not be renumbered after use. New observations take the next unused number even if placed earlier in the anatomical hierarchy.

Permitted `Observation status` values are:

- `Observed`
- `Not observed`
- `Not examined`
- `Uncertain`
- `Absent`

Use `Absent` only when the relevant structure was adequately examined and its absence was established.

## Measurements

Keep individual measurements rather than replacing them with only a range or mean:

```markdown
- Individual measurements:
  - 4.2 mm
  - 4.4 mm
  - 4.3 mm
```

Record landmarks, calibration, instrument, and exclusions under `Method` or `Uncertainty or limitation`.

## Preparations

Use a stable preparation identifier:

```markdown
### PREP-001 — Temporary wing mount

- Material: Right wing
- Previous state: Attached to intact specimen
- New state: Detached and temporarily mounted
- Preparation type: Temporary
- Method and medium: Water mount under coverslip
- Orientation: Dorsal surface uppermost
- Purpose: Examine venation and membrane vestiture
- Can it be revisited?: No
- Related observations: OBS-010, OBS-011
- Limitations: Mount lost after examination
```

## Corrections

Correct the relevant structured field, but add a dated revision-history entry describing the substantive correction. Do not leave a known incorrect value as the current observation, and do not silently restore it later.

## Parser expectations

A future importer may rely on:

- YAML metadata keys;
- the stable level-two headings;
- observation identifiers beginning `OBS-`;
- preparation identifiers beginning `PREP-`;
- the field labels shown in the template;
- indentation of repeated individual measurements.

Additional explanatory prose is permitted. An importer must preserve or report text it cannot map rather than silently discarding it.
