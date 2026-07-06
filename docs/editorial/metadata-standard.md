# Recipe Metadata Standard

Every recipe should begin with YAML front matter. Metadata makes the cookbook easier to search, review, filter, and maintain over time.

## Required Fields

```yaml
title: Recipe Name
status: draft | testing | approved | archived
category: dinner | side | sauce | breakfast | work-box | dessert | staple
season: spring | summer | fall | winter | all-season
source: Kester family rotation
created: YYYY-MM-DD
last_tested: YYYY-MM-DD
approved: true | false
anylist: true | false
```

## Recommended Fields

```yaml
tags:
  - weeknight
  - grill
  - make-ahead
work_box: yes | no | with-modification
effort: low | medium | high
servings: 4
leftover_quality: poor | okay | good | excellent
```

## Status Definitions

Use these values consistently:

- `draft`: Not cooked or not yet documented enough for testing.
- `testing`: Cooked or scheduled in a rotation, still being evaluated.
- `approved`: Permanent family cookbook recipe.
- `archived`: Retired from active use.

## Tag Guidance

Tags should describe how the family uses the recipe, not just what cuisine it resembles.

Good tags:

- `summer`
- `grill`
- `work-box-friendly`
- `low-effort`
- `company-worthy`
- `uses-leftover-chicken`

Avoid vague tags:

- `good`
- `easy` without context
- `favorite` unless it is truly a family favorite

## AnyList Field

Use `anylist: true` only when the recipe is clean enough to import from the published site. Draft notes, testing clutter, and ambiguous ingredients should be cleaned up first.
