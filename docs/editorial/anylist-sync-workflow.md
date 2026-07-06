# Publishing and AnyList Cooking Workflow

GitHub is the source of truth for recipe content. The cookbook website is the published reference. AnyList is the practical cooking tool used in the kitchen.

Architecture 1.1 treats AnyList as part of recipe testing, not merely a final export destination.

## Workflow

```text
GitHub recipe
  ↓
Published cookbook page
  ↓
Imported into AnyList
  ↓
Cooked from AnyList
  ↓
Cooking notes captured
  ↓
GitHub recipe revised
```

The goal is not automation. The goal is to make it easy to see whether the AnyList copy matches the cookbook and whether the recipe actually works in the kitchen.

## Metadata Fields

Each recipe should include website and AnyList blocks:

```yaml
version: 1.0.0

website:
  published: true
  published_date: YYYY-MM-DD
  canonical_url: https://cookbook.connellkesters.com/path-to-recipe/

anylist:
  ready: true
  imported: false
  imported_date:
  imported_version:
  list_name: Kester Family Cookbook
  recipe_name:
  notes:
```

## AnyList Readiness

A recipe is ready for AnyList when:

- Ingredients are clear enough to shop from.
- Instructions are clean enough to cook from.
- Timing is useful enough for kitchen use.
- Draft notes and editorial clutter have been removed or moved to revision notes.
- The published cookbook URL works, if importing from the site.

A recipe may be imported into AnyList while still in `testing` status. Cooking from AnyList may be part of the test.

When those conditions are met, set:

```yaml
anylist:
  ready: true
```

## After Importing into AnyList

After manually importing the recipe into AnyList, update the metadata:

```yaml
anylist:
  ready: true
  imported: true
  imported_date: YYYY-MM-DD
  imported_version: 1.0.0
  list_name: Kester Family Cookbook
  recipe_name: Recipe Name
```

## Cooking from AnyList

When a recipe is cooked from AnyList, capture feedback in the recipe's Cooking Feedback section.

Useful notes include:

- Did the step order work?
- Were the timers helpful?
- Were ingredient amounts clear?
- Was anything hard to read while cooking?
- Did the recipe need more or less detail?
- Should the GitHub recipe be revised before the next import?

## How to Spot a Recipe That Needs Re-Import

A recipe probably needs re-import when the cookbook version is newer than the imported AnyList version.

Example:

```yaml
version: 1.2.0

anylist:
  imported: true
  imported_version: 1.0.0
```

This does not automatically detect a mismatch. It gives us a simple manual way to spot that GitHub has changed since the AnyList copy was imported.

## Suggested AnyList Note

When possible, include this note inside the AnyList recipe:

```text
Source: Kester Family Cookbook
Version: 1.0.0
URL: https://cookbook.connellkesters.com/path-to-recipe/
```

This gives a quick way to compare the AnyList copy against GitHub.

## Editorial Rule

Do not treat AnyList as the permanent archive. If a recipe is changed in AnyList during real cooking, bring the change back into GitHub so the cookbook remains the source of truth.
