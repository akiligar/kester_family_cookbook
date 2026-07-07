# Metadata Reference

This document is the authoritative reference for every YAML metadata field used in cookbook recipes.

The recipe template defines the structure. This guide explains what each field means, when to use it, and acceptable values.

## Identity

| Field | Purpose |
| --- | --- |
| `title` | Canonical recipe name. |
| `status` | `draft`, `testing`, `approved`, or `archived`. |
| `version` | Semantic recipe version (e.g. `1.2.0`). |

## Classification

| Field | Allowed Values |
| --- | --- |
| `category` | `main-dish`, `side-dish`, `sauce`, `breakfast`, `work-box`, `dessert`, `staple` |
| `protein` | `beef`, `chicken`, `pork`, `seafood`, `turkey`, `vegetarian`, `mixed`, `none` |
| `rotation_role` | `weeknight-dinner`, `weekend-dinner`, `work-box`, `side`, `sauce`, `breakfast`, `company`, `holiday`, `staple` |
| `season` | `spring`, `summer`, `fall`, `winter`, `all-season` |

## Source

- `source` – Where the recipe originated.
- `source_url` – Original reference, if applicable.

## Lifecycle

- `created`
- `last_tested`
- `approved`
- `approved_date`

GitHub is the source of truth. A recipe becomes permanent when it reaches `approved: true`.

## Website

Tracks publication to the MkDocs website.

- `published`
- `published_date`
- `canonical_url`

## AnyList

Tracks the relationship between GitHub and AnyList.

- `ready` – Suitable for import.
- `imported` – Imported into AnyList.
- `imported_date`
- `imported_version` – Version currently represented in AnyList.
- `list_name`
- `recipe_name`
- `notes`

A recipe requires re-import whenever `version` is newer than `imported_version`.

## Cooking

- `servings`
- `prep_time`
- `cook_time`
- `total_time`
- `effort`
- `make_ahead`

## Practical Use

- `work_box`
- `leftover_quality`
- `freezer_friendly`
- `kid_friendly`

These fields describe how the family actually uses the recipe, not how a generic cookbook might classify it.

## Planned Transformation

The `transformation` block documents intentional second meals.

Fields:

- `has_transformation`
- `transformation_name`
- `transformation_type`
- `transformation_timing`
- `transformation_url`
- `work_box_friendly`

A transformation is not simply leftovers—it is a planned follow-up meal.

## Planning Fields

### `primary_ingredients`

List only ingredients that drive shopping and meal planning.

### `equipment`

List notable equipment required to prepare the recipe.

### `tags`

Tags should improve discovery, such as:

- `summer`
- `grill`
- `blackstone`
- `planned-transformation`
- `work-box-friendly`
- `company-worthy`

## Editorial Rules

- Every approved recipe should include the complete metadata block.
- Metadata should describe how the Kester family cooks, not generic cookbook assumptions.
- `version` and the version embedded in the recipe description must always match.
- GitHub metadata is the authoritative source for recipe status and publication state.