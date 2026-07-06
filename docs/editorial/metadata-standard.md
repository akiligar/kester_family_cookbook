# Recipe Metadata Standard

Every recipe should begin with YAML front matter. Metadata turns each recipe into a reusable recipe card that can later be searched, filtered, indexed, and reviewed.

The metadata should describe how the Kester family actually uses the recipe, not just what kind of dish it is.

## Standard Recipe Card

Use this full metadata block for new recipes.

```yaml
title: Recipe Name
status: draft | testing | approved | archived
version: 0.1.0
category: dinner | side | sauce | breakfast | work-box | dessert | staple
rotation_role: weeknight-dinner | weekend-dinner | work-box | side | sauce | breakfast | company | holiday | staple
season: spring | summer | fall | winter | all-season
source: Kester family rotation
source_url:
created: YYYY-MM-DD
last_tested: YYYY-MM-DD
approved: false
approved_date:

website:
  published: false
  published_date:
  canonical_url:

anylist:
  ready: false
  imported: false
  imported_date:
  imported_version:
  list_name: Kester Family Cookbook
  recipe_name:
  notes:

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
version: 0.1.0
category: dinner | side | sauce | breakfast | work-box | dessert | staple
rotation_role: weeknight-dinner | weekend-dinner | work-box | side | sauce | breakfast | company | holiday | staple
season: spring | summer | fall | winter | all-season
created: YYYY-MM-DD
last_tested: YYYY-MM-DD
approved: false
website:
  published: false
anylist:
  ready: false
  imported: false
  imported_date:
  imported_version:
  list_name: Kester Family Cookbook
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

### `version`

Use semantic-style recipe versions.

- Start drafts at `0.1.0`.
- Use `1.0.0` when a recipe is first approved.
- Increment the version when the ingredients, timing, method, or work-box notes meaningfully change.
- Minor wording edits do not need a version change unless they affect cooking or AnyList import clarity.

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

### `website`

The website block tracks whether the recipe has been published from GitHub to the cookbook site.

Use `website.published: true` only after the recipe is visible on the published cookbook site.

### `anylist`

The AnyList block tracks whether the published recipe has been imported into AnyList.

Use these rules:

- `ready: true` means the recipe is clean enough to import.
- `imported: true` means it has been imported into AnyList.
- `imported_version` records the recipe version that was imported.
- If `version` is newer than `imported_version`, the recipe needs to be re-imported.
- `recipe_name` should match the name used inside AnyList if it differs from the cookbook title.
- `notes` can record manual details, such as duplicate cleanup or import quirks.

A recipe is current in AnyList only when:

```yaml
version: 1.2.0
anylist:
  imported: true
  imported_version: 1.2.0
```

If the versions differ, GitHub is newer than AnyList.

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
version: 0.1.0
category: dinner
rotation_role: weeknight-dinner
season: all-season
created: YYYY-MM-DD
approved: false
website:
  published: false
anylist:
  ready: false
  imported: false
servings: 4
effort: medium
work_box: untested
leftover_quality: untested
tags:
  - testing
```

Before a recipe becomes approved, it should be upgraded to the full standard recipe card.
