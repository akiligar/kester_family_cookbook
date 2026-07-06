# Dinner-to-Transformation Workflow

Architecture 1.2 recognizes that some recipes are not single meals. They are planned meal systems.

```text
Dinner
  ↓
Intentional next meal
```

This matters for the Kester Family Cookbook because many dinners should support work boxes, graveyard-shift meals, and practical next-day eating.

## Leftovers vs. Transformations

Leftovers are passive. They are what remains after dinner.

Transformations are intentional. They are planned second meals created from the first meal.

Examples:

- Grilled flank steak becomes chimichurri steak salad.
- Mediterranean chicken becomes a wrap.
- Pork shoulder becomes rice bowls or tacos.
- Roast vegetables become breakfast hash.

## When to Use a Planned Transformation

Use a planned transformation when:

- Dinner intentionally produces components for another meal.
- The next meal is meaningfully different from dinner.
- The transformation improves work-box or 2:00 AM eating.
- Packing, slicing, storing, or holding ingredients separately matters.
- The second meal would fail without planning.

Do not force every recipe to have a transformation. Some meals only need ordinary leftover notes.

## Required Transformation Details

A transformation-ready recipe should answer:

- What is the next meal called?
- What dinner components are intentionally saved?
- What additional ingredients are needed?
- What must be packed or stored separately?
- What should be done before leaving for work?
- What should happen at work or at 2:00 AM?
- Did the transformation actually work?

## Metadata

Recipes with planned transformations should include:

```yaml
transformation:
  has_transformation: true
  transformation_name: Chimichurri Steak Salad
  transformation_type: salad
  transformation_timing: work-box
  transformation_url:
  work_box_friendly: true
```

## Editorial Rule

A planned transformation should be treated as part of the recipe's value, not as a casual leftover suggestion.

A dinner that reliably creates a strong second meal may deserve a place in the cookbook even if the dinner alone is simple.

## Testing Rule

A transformation recipe is not fully tested until both parts have been evaluated:

1. The dinner worked.
2. The transformation worked as the next meal.

If the dinner is good but the transformation fails, the recipe may still be useful, but it should not be marked as transformation-proven.
