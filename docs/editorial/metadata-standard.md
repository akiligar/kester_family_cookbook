# Recipe Metadata Standard

Every recipe should begin with YAML front matter. Metadata turns each recipe into a reusable recipe card that can later be searched, filtered, indexed, and reviewed.

The metadata should describe how the Kester family actually uses the recipe, not just what kind of dish it is.

## Standard Recipe Card

Use this full metadata block for new recipes.

```yaml
title: Recipe Name
status: draft | testing | approved | archived
category: dinner | side | sauce | breakfast | work-box | dessert | staple
rotation_role: weeknight-dinner | weekend-dinner | work-box | side | sauce | breakfast | company | holiday | staple
season: spring | summer | fall | winter | all-season
source: Kester family rotation
source_url:
created: YYYY-MM-DD
last_tested: YYYY-MM-DD
approved: false
approved_date:
anylist: false

servings: 4
prep_time: 00:00
cook_time: 00:00
total_time: 00:00
effort: low | medium | high
make_ahead: yes | no | partial

work_box: yes | no | with-modification
leftover_quality: poor | okay | good | excellent
freezer_friendly: yes | no | untested
kid_friendly: yes | no | mixed | untested

primary_ingredients:
  - ingredient
equipment:
  - equipment item
tags:
  - weeknight
  - summer
  - grill
```

## Required Fields

Every recipe should include these fields:

```yaml
title: Recipe Name
status: draft | testing | approved | archived
category: dinner | side | sauce | breakfast | work-box | dessert | staple
rotation_role: weeknight-dinner | weekend-dinner | work-box | side | sauce | breakfast | company | holiday | staple
season: spring | summer | fall | winter | all-season
created: YYYY-MM-DD
last_tested: YYYY-MM-DD
approved: false
anylist: false
servings: 4
prep_time: 00:00
cook_time: 00:00
total_time: 00:00
effort: low | medium | high
work_box: yes | no | with-modification
leftover_quality: poor | okay | good | excellent
tags:
  - tag
```

## Field Definitions

### `status`

Use one of these values:

- `draft`: Not cooked or not yet documented enough for testing.
- `testing`: Cooked or scheduled in a rotation, still being evaluated.
- `approved`: Permanent family cookbook recipe.
- `archived`: Retired from active use.

### `rotation_role`

Use this to describe the job the recipe performs in the family rotation.

Examples:

- `weeknight-dinner`
- `weekend-dinner`
- `work-box`
- `side`
- `sauce`
- `breakfast`
- `company`
- `holiday`
- `staple`

### `season`

Use the season when the family actually wants to cook the recipe.

A tomato-heavy pasta may technically be possible all year, but if it only makes sense with summer tomatoes, mark it `summer`.

### `anylist`

Use `anylist: true` only when the recipe is clean enough to import from the published site. Draft notes, testing clutter, and ambiguous ingredients should be cleaned up first.

### `primary_ingredients`

Use this for planning and waste reduction. Do not list every pantry item. Focus on ingredients that drive shopping decisions.

Good examples:

- flank steak
- chicken thighs
- asparagus
- corn
- cilantro

Poor examples:

- salt
- pepper
- olive oil, unless it is unusually central to the recipe

### `tags`

Tags should describe how the family uses the recipe, not just what cuisine it resembles.

Good tags:

- `summer`
- `grill`
- `work-box-friendly`
- `low-effort`
- `company-worthy`
- `uses-leftover-chicken`
- `graveyard-shift`
- `kid-friendly`

Avoid vague tags:

- `good`
- `easy` without context
- `favorite` unless it is truly a family favorite

## Minimal Draft Metadata

For rough drafts, this smaller block is acceptable:

```yaml
title: Recipe Name
status: draft
category: dinner
rotation_role: weeknight-dinner
season: all-season
created: YYYY-MM-DD
approved: false
anylist: false
servings: 4
effort: medium
work_box: untested
leftover_quality: untested
tags:
  - testing
```

Before a recipe becomes approved, it should be upgraded to the full standard recipe card.
