Project Documentation

This directory contains the internal documentation used to develop and maintain the Kester Family Cookbook.

Unlike the docs/ directory, the contents of project/ are not published to the cookbook website. These documents describe how the cookbook is built, organized, and maintained rather than how recipes are prepared.

Purpose

The cookbook has two audiences:

* Cookbook users — People looking for recipes, cooking instructions, and reference material.
* Cookbook editors — People maintaining the cookbook, refining recipes, and improving the project over time.

The docs/ directory serves cookbook users.

The project/ directory serves cookbook editors.

Directory Structure

project/
├── architecture/
│   Long-term design decisions and architecture revisions.
│
├── workflow/
│   Editorial and operational workflows, including recipe development,
│   publishing, and AnyList processes.
│
├── operations/
│   GitHub, Cloudflare, deployment, and other technical documentation.
│
└── planning/
    Future ideas, backlog items, and project planning documents.

Editorial Philosophy

The goal of the Kester Family Cookbook is not simply to collect recipes.

The goal is to build a permanent family cookbook that reflects how the Kester family actually cooks.

Recipes should become more accurate and more useful over time through testing, revision, and editorial review.

Whenever possible:

* Improve existing recipes before adding new ones.
* Capture long-term editorial decisions.
* Prefer consistency over novelty.
* Treat GitHub as the authoritative source for cookbook content.
* Keep operational documentation separate from the published cookbook.

Relationship to the Published Site

Only documents under docs/ are intended for publication through MkDocs.

Documents in project/ are internal references and should not be linked from the published cookbook navigation.

Source of Truth

* GitHub is the permanent source of truth.
* Cloudflare Pages publishes the cookbook website.
* AnyList is the preferred cooking interface and should reflect the approved recipe versions maintained in GitHub.