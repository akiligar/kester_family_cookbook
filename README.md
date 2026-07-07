# Kester Family Cookbook Project Documentation

> **Purpose:** This directory contains the internal documentation used to develop, maintain, and improve the Kester Family Cookbook.

---

## Overview

The repository is intentionally divided into two distinct areas:

| Directory | Purpose | Published |
|-----------|---------|:---------:|
| `docs/` | Cookbook content, recipes, and editorial references | ✅ Yes |
| `project/` | Internal project documentation and operational guidance | ❌ No |

The `docs/` directory contains the content that is published through MkDocs as the cookbook website.

The `project/` directory contains documentation for maintaining the cookbook itself, including architecture decisions, workflows, planning documents, and operational references.

---

## Directory Structure

```text
project/
├── architecture/
│   ├── Architecture revisions
│   └── Long-term design decisions
│
├── workflow/
│   ├── Editorial workflows
│   ├── Recipe development process
│   └── Publishing workflows
│
├── operations/
│   ├── GitHub documentation
│   ├── Cloudflare deployment
│   └── Technical operations
│
└── planning/
    ├── Future enhancements
    ├── Project backlog
    └── Strategic planning
```

---

## Project Philosophy

The objective of this project is **not** to collect recipes.

The objective is to build and maintain a permanent cookbook that accurately reflects how the Kester family cooks.

Editorial decisions should prioritize:

- Improving existing recipes before adding new ones.
- Documenting long-term decisions rather than temporary discussions.
- Maintaining consistency throughout the cookbook.
- Treating GitHub as the authoritative source for all cookbook content.
- Separating cookbook content from project management documentation.

---

## Publishing Policy

### Published (`docs/`)

- Recipes
- Recipe indexes
- Editorial references
- Family Preferences
- Change Log
- Public cookbook documentation

### Internal (`project/`)

- Architecture documents
- Workflow documentation
- Operational procedures
- Planning documents
- Technical notes
- Future design proposals

---

## Project Workflow

```text
VS Code
    │
    ▼
Local Git Repository
    │
    ▼
GitHub (Source of Truth)
    │
    ▼
Cloudflare Pages
    │
    ▼
Published Cookbook
    │
    ▼
AnyList
```

---

## Source of Truth

| Component | Responsibility |
|-----------|----------------|
| **GitHub** | Permanent repository and authoritative cookbook source |
| **MkDocs** | Static site generation |
| **Cloudflare Pages** | Website hosting and deployment |
| **AnyList** | Preferred cooking interface for approved recipes |

---

## Guiding Principle

> **Every permanent decision should have a permanent home.**
>
> Recipes belong in the cookbook.
>
> Editorial guidance belongs in the published editorial documentation.
>
> Project operations belong in this directory.