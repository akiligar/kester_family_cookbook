# AnyList Sync Workflow

GitHub is the source of truth for recipe content. AnyList is the shopping and practical cooking tool.

This workflow tracks whether AnyList has the current version of each approved recipe.

## Metadata Fields

Each recipe should include an AnyList block:

```yaml
version: 1.0.0

anylist:
  ready: true
  imported: false
  imported_date:
  imported_version:
  list_name: Kester Family Cookbook
  recipe_name:
  notes:
```

## Import Rules

A recipe is ready for AnyList when:

- The recipe is approved or intentionally ready for testing in AnyList.
- Ingredients are clear enough to shop from.
- Instructions are clean enough to cook from.
- Draft notes and editorial clutter have been removed or moved to revision notes.
- The published cookbook URL works.

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

## How to Know a Recipe Needs Re-Import

A recipe needs re-import when the cookbook version is newer than the imported AnyList version.

Example:

```yaml
version: 1.2.0

anylist:
  imported: true
  imported_version: 1.0.0
```

This means the website has changed since the recipe was imported into AnyList.

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
