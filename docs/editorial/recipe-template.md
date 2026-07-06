# Recipe Template

This is the canonical template for recipes in the Kester Family Cookbook.

Use it when creating new recipes for GitHub, the published cookbook site, and AnyList import.

A recipe must work in two ways:

1. As a clean cooking document for AnyList.
2. As a living cookbook record with testing notes, transformation notes, and revision history.

To protect AnyList import, the top of the visible recipe should stay simple and conventional:

```text
Title
Description
Servings and Time
Ingredients
Instructions
```

Editorial content belongs after the cooking instructions.

## Copy/Paste Template

```markdown
---
title: Recipe Name
status: draft | testing | approved | archived
version: 0.1.0
category: main-dish | side-dish | sauce | breakfast | work-box | dessert | staple
protein: beef | chicken | pork | seafood | turkey | vegetarian | mixed | none
rotation_role: weeknight-dinner | weekend-dinner | work-box | side-dish | sauce | breakfast | company | holiday | staple
season: spring | summer | fall | winter | all-season
source: Kester family rotation
source_url:
created: YYYY-MM-DD
last_tested:
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
  transformation_type: cold | handheld | bowl | soup | reheated | breakfast | salad | mixed | other
  transformation_timing: next-day | same-night | work-box | planned-leftover
  transformation_url:
  work_box_friendly: false

primary_ingredients:
  - ingredient
equipment:
  - equipment item
tags:
  - testing
---

<article itemscope itemtype="https://schema.org/Recipe" markdown="1">

# <span itemprop="name">Recipe Name</span>

<span itemprop="description">Brief one- or two-sentence recipe summary. Version: 0.1.0.</span>

<meta itemprop="recipeCategory" content="Main dish">
<meta itemprop="recipeCuisine" content="American">
<meta itemprop="prepTime" content="PT00M">
<meta itemprop="cookTime" content="PT00M">
<meta itemprop="totalTime" content="PT00M">
<meta itemprop="recipeYield" content="4 servings">
<meta itemprop="keywords" content="testing">

## Servings and Time

- Servings: <span itemprop="recipeYield">4</span>
- Prep time: 00 minutes
- Cook time: 00 minutes
- Total time: about 00 minutes

## Ingredients

### Main Component

- <span itemprop="recipeIngredient">Ingredient 1</span>
- <span itemprop="recipeIngredient">Ingredient 2</span>

### Sauce / Dressing / Secondary Component

- <span itemprop="recipeIngredient">Ingredient 1</span>
- <span itemprop="recipeIngredient">Ingredient 2</span>

## Instructions

### Prepare

<ol>
<li itemprop="recipeInstructions" itemscope itemtype="https://schema.org/HowToStep"><span itemprop="text">Step one.</span></li>
<li itemprop="recipeInstructions" itemscope itemtype="https://schema.org/HowToStep"><span itemprop="text">Step two.</span></li>
</ol>

### Cook

<ol>
<li itemprop="recipeInstructions" itemscope itemtype="https://schema.org/HowToStep"><span itemprop="text">Step one.</span></li>
<li itemprop="recipeInstructions" itemscope itemtype="https://schema.org/HowToStep"><span itemprop="text">Step two.</span></li>
</ol>

### Serve

<ol>
<li itemprop="recipeInstructions" itemscope itemtype="https://schema.org/HowToStep"><span itemprop="text">Step one.</span></li>
</ol>

## Planned Transformation

Use this section only when the dinner is intentionally designed to become a second meal. If there is no planned transformation, write: None.

### Transformation Meal

Name the next meal and explain why the dinner was designed to become it.

### Additional Ingredients

- Ingredient 1
- Ingredient 2

### Before Leaving for Work

1. Pack, slice, portion, chill, or separate ingredients as needed.
2. Keep sauces, greens, crunchy toppings, and reheated items separate when appropriate.

### At Work / At 2:00 AM

1. Assemble, reheat, dress, or eat the transformation meal.

## Make-Ahead Notes

- Note what can be prepared earlier.
- Note what should not be prepared too early.

## Storage and Leftovers

- Note how to store leftovers.
- Note whether leftovers are good, limited, or not useful.

## AnyList Cooking Notes

Suggested note to include inside AnyList:

```text
Source: Kester Family Cookbook
Version: 0.1.0
URL: https://cookbook.connellkesters.com/path-to-recipe/
```

After importing into AnyList, update the `anylist` metadata block above.

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

</article>
```

## Required AnyList Import Structure

For AnyList and similar recipe import tools:

- Use one visible `#` title.
- Wrap the visible recipe body in `<article itemscope itemtype="https://schema.org/Recipe" markdown="1">`.
- Mark the title with `itemprop="name"`.
- Mark the description with `itemprop="description"`.
- Include `Version: x.y.z.` inside the visible description.
- Use `## Ingredients` before `## Instructions`.
- Mark every ingredient with `itemprop="recipeIngredient"`.
- Mark every cooking step with `itemprop="recipeInstructions"` and `https://schema.org/HowToStep`.
- Keep testing notes, family notes, revision notes, and editorial explanations after the cooking instructions.

## Version Rule

Every recipe has two visible version references:

1. YAML metadata:

```yaml
version: 0.1.0
```

2. AnyList-visible description:

```text
Version: 0.1.0.
```

These must match. If the recipe version changes, update both places.

## Category and Protein Rules

Use `main-dish` for dinner entrees. Do not use `dinner` as a category.

Use `side-dish` for sides. Do not use `side` as a category.

For `protein`, use one of:

```text
beef | chicken | pork | seafood | turkey | vegetarian | mixed | none
```

Use `none` for side dishes, sauces, staples, and recipes without a central protein.

## Planned Transformation Rule

A transformation is not a leftover note.

- Leftovers are what remains.
- A planned transformation is the second meal the dinner is intentionally designed to become.

Only set `transformation.has_transformation: true` when the second meal is intentionally planned and documented.
