# Recipe Template

Use this template for recipes that may enter the permanent cookbook.

Recipes must work in two formats:

1. The published cookbook website.
2. AnyList import and cooking.

For import reliability, keep the visible recipe structure simple and conventional near the top of the page: title, summary, servings/time, ingredients, and instructions. Put editorial notes after the cooking instructions.

```markdown
---
title: Recipe Name
status: draft | testing | approved | archived
version: 0.1.0
category: main-dish | side-dish | sauce | breakfast | work-box | dessert | staple
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

transformation:
  has_transformation: false
  transformation_name:
  transformation_type: cold | handheld | bowl | soup | reheated | breakfast | salad | other
  transformation_timing: next-day | same-night | work-box | planned-leftover
  transformation_url:
  work_box_friendly: false

primary_ingredients:
  - ingredient
equipment:
  - equipment item
tags:
  - weeknight
  - testing
---

# Recipe Name

Brief one- or two-sentence recipe summary.

## Servings and Time

- Servings: 4
- Prep time: 00:00
- Cook time: 00:00
- Total time: 00:00

## Ingredients

Keep this section clean. Avoid editorial notes, testing notes, and optional commentary.

### Main Component

- Ingredient 1
- Ingredient 2

### Sauce / Dressing / Secondary Component

- Ingredient 1
- Ingredient 2

## Instructions

Keep this section cookable. Avoid long explanations that interfere with AnyList timers and step parsing.

### Prepare

1. Step one.
2. Step two.

### Cook

1. Step one.
2. Step two.

### Serve

1. Step one.

## Planned Transformation

A transformation is not a leftover note. It is the planned second meal this recipe is designed to become.

### Transformation Meal

Name the next meal and explain why the dinner was designed to become it.

### Additional Ingredients

- Ingredient 1
- Ingredient 2

### Before Leaving for Work

List what should be sliced, packed, portioned, chilled, or held separately before work.

### At Work / At 2:00 AM

Explain how to assemble, reheat, dress, or eat the transformation meal.

## Make-Ahead Notes

What can be done earlier?

## Storage and Leftovers

What usable leftovers does this create? If it does not work well as leftovers, say so.

## AnyList Cooking Notes

When this recipe is imported into AnyList, update the metadata block above.

Suggested note to include inside AnyList:

```text
Source: Kester Family Cookbook
Version: 0.1.0
URL: https://cookbook.connellkesters.com/path-to-recipe/
```

After cooking from AnyList, capture what worked or failed in the Cooking Feedback section below.

## Why This Recipe Belongs

Briefly explain why this recipe deserves a place in the family cookbook. For drafts and testing recipes, explain what role it might fill.

## Status and Testing Notes

Current status: draft | testing | approved | archived

- Date tested:
- Result:
- Next adjustment:

## Cooking Feedback

- YYYY-MM-DD: Cooked from planned recipe / website / AnyList. Note what worked, what was confusing, and what should change next time.

## Transformation Feedback

- YYYY-MM-DD: Note whether the transformation worked, what was missing, and what should change next time.

## Variations

Only include variations the family would realistically cook.

## What Matters

List details that should not be changed because they affect the result.

## Revision Notes

- YYYY-MM-DD: Initial version.
```

## Import Compatibility Rules

For AnyList and similar recipe import tools:

- Use `# Recipe Name` as the visible recipe title.
- Use `## Ingredients` for the ingredient list.
- Use `## Instructions` for cooking steps.
- Put ingredients before instructions.
- Keep editorial notes after the cooking instructions.
- Avoid putting testing status, family notes, or workflow notes between the title and the ingredients.
- Use ordinary ingredient bullets and numbered instruction steps.
- Prefer `Servings and Time` over a complex recipe-information table.
