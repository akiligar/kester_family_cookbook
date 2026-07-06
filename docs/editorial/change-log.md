# Change Log

Use this page to summarize meaningful cookbook changes and help re-orient the project after a break.

The changelog should answer:

- What changed?
- Why did it change?
- Where should I look next?
- What is the current working model?

## Current Project State

The Kester Family Cookbook is now a GitHub-backed MkDocs cookbook published at:

<https://cookbook.connellkesters.com/>

Current architecture version: **Architecture 1.2**

Current working model:

```text
Rotation planning
  ↓
Recipe testing
  ↓
Website publishing
  ↓
AnyList cooking
  ↓
Cooking and transformation feedback
  ↓
GitHub cookbook revision
```

GitHub remains the source of truth. The website is the published reference. AnyList is the kitchen cooking tool.

## Architecture History

### Architecture 1.0 — Cookbook Foundation

Established GitHub as the source of truth and MkDocs as the cookbook publishing system.

Key concepts:

- GitHub stores permanent cookbook content.
- MkDocs publishes the cookbook website.
- Recipes live as Markdown files.
- Editorial quality matters more than recipe quantity.

Where to look:

- [Recipe Standards](recipe-standards.md)
- [Recipe Template](recipe-template.md)
- [Metadata Standard](metadata-standard.md)

### Architecture 1.1 — AnyList as Kitchen Runtime

Refined the workflow after recognizing that AnyList is not merely an export destination. It is the tool used while cooking.

Key concepts:

- Recipes may enter AnyList while still in testing.
- A recipe should be cooked successfully from the kitchen format before approval.
- AnyList sync tracking is manual, not automated.
- Version fields help spot when GitHub has changed since the AnyList copy was imported.

Where to look:

- [Publishing and AnyList Cooking](anylist-sync-workflow.md)
- [Recipe Lifecycle](recipe-lifecycle.md)

### Architecture 1.2 — Dinner-to-Transformation Systems

Added support for recipes designed to become intentional second meals.

Key concepts:

- Leftovers are passive.
- Transformations are planned.
- Some recipes are meal systems: dinner plus an intentional next meal.
- A transformation recipe is not fully tested until both the dinner and the transformation have been evaluated.

Where to look:

- [Transformation Workflow](transformation-workflow.md)
- [Recipe Template](recipe-template.md)
- [Metadata Standard](metadata-standard.md)

## 2026-07-06

### Implemented Architecture 1.2

Added dinner-to-transformation support as a first-class cookbook concept.

Changed:

- Added transformation metadata fields.
- Added a Planned Transformation section to the recipe template.
- Added transformation feedback guidance.
- Added the Transformation Workflow editorial page.
- Updated recipe standards to distinguish leftovers from transformations.
- Added Transformation Workflow to site navigation.

Why it matters:

This supports the actual meal-planning pattern where dinner is intentionally designed to become a second meal, especially for work boxes and 2:00 AM meals.

### Implemented Architecture 1.1

Updated the architecture to reflect that AnyList is the practical cooking tool.

Changed:

- Updated the recipe lifecycle to include publishing, AnyList import, cooking from AnyList, and feedback.
- Updated recipe standards so approval depends on practical cooking success.
- Added AnyList cooking notes to the recipe template.
- Added a Cooking Feedback section to the recipe template.
- Renamed the navigation entry to Publishing and AnyList Cooking.

Why it matters:

The cookbook should not merely publish recipes. It should support the way the family actually cooks.

### Added AnyList Tracking Metadata

Added structured metadata for manual AnyList tracking.

Changed:

- Added recipe `version`.
- Added `website:` metadata.
- Added structured `anylist:` metadata.
- Added `imported_version` to make version mismatches easier to spot.

Why it matters:

This does not automate AnyList sync, but it makes it easier to know whether the AnyList copy reflects the current GitHub recipe.

### Added Standardized Recipe Metadata

Expanded the recipe metadata into a standardized recipe card.

Changed:

- Added timing fields.
- Added effort, make-ahead, work-box, leftover, freezer, and kid-friendly fields.
- Added primary ingredients, equipment, and tags.

Why it matters:

This makes recipes easier to search, review, classify, and convert into practical cooking tools.

### Built the Editorial Architecture

Added the major editorial pages that define how the cookbook should operate.

Changed:

- Added Recipe Lifecycle.
- Added Recipe Metadata Standard.
- Added Rotation-to-Recipe Workflow.
- Added Seasonal Index.
- Added Ingredient Index.
- Added Work Box Index.
- Strengthened Recipe Standards.
- Expanded the Editorial index page.

Why it matters:

The cookbook is now an editorial system, not just a folder of recipes.

### Completed Publishing Setup

Completed the infrastructure setup for the published cookbook.

Changed:

- Set the canonical site URL to `https://cookbook.connellkesters.com/`.
- Connected the GitHub-backed cookbook to Cloudflare publishing.
- Verified that MkDocs builds successfully.

Why it matters:

The cookbook can now be published and used as the basis for AnyList imports.

## 2026-07-05

### Created Initial GitHub/MkDocs Cookbook Structure

Created the starter structure for the Kester Family Cookbook.

Changed:

- Added MkDocs configuration.
- Added recipe folders.
- Added planning, editorial, and reference sections.
- Added initial recipe template.
- Added starter recipe standards.
- Added pantry and equipment reference pages.

Why it matters:

This established the permanent cookbook repository and basic site structure.

## Changelog Rules

Add an entry when a change affects:

- Cookbook architecture.
- Recipe lifecycle.
- Metadata standards.
- Publishing workflow.
- AnyList workflow.
- Transformation workflow.
- Navigation or organization.
- A recipe becoming approved, archived, or materially revised.

Minor copy edits do not need changelog entries unless they affect cooking, publishing, or project direction.
