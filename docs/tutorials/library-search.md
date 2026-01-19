---
layout: default
title: Library Search
nav_order: 5
---

# Library Search

Find and share community-created TSWoW modules.

[**Browse the Library**](https://tswow-library-search.bold-term-1c95.workers.dev/){: .btn .btn-primary }

---

## Publishing Your Module

To make your module discoverable in the library search, follow these two steps:

### 1. Add the GitHub Topic

The library search finds modules by looking for repositories tagged with `tswow-module`:

1. Go to your repository on GitHub
2. Click the gear icon next to "About" in the right sidebar
3. Add `tswow-module` to the Topics field
4. Save changes

Your repository will be indexed automatically within a few hours.

### 2. Structure Your Repository

The search supports two layouts depending on whether you're publishing one module or several.

**Single module** — Place your endpoint folders at the repository root:

```
myname-mymodule/
├── datascripts/
├── livescripts/
├── assets/
└── README.md
```

**Multiple modules** — Each top-level folder becomes a separate module:

```
my-module-collection/
├── myname-module-one/
│   ├── datascripts/
│   └── README.md
├── myname-module-two/
│   ├── livescripts/
│   └── README.md
└── README.md
```

Common directories like `.github`, `node_modules`, `docs`, `tests`, `src`, `lib`, and `examples` are automatically excluded from module detection.

---

## Optimizing for Search

The library uses semantic search, which means it understands the meaning behind queries rather than just matching keywords.

### Indexed Content

The search indexes the following from your repository:

| Content | Notes |
|---------|-------|
| Repository name | Use a descriptive name |
| GitHub description | The "About" text on your repo |
| GitHub topics | All topics, not just `tswow-module` |
| README content | First ~5,000 characters |

### Tips for Discoverability

**Write a strong GitHub description.** This appears prominently in search results. Be specific about what your module does.

**Add relevant topics.** Go beyond `tswow-module` — add topics like `custom-class`, `profession`, `dungeon`, `quests`, or whatever describes your content.

**Document your README well.** Explain what the module does, what features it includes, and how to use it. Good documentation helps both search ranking and users evaluating your module.

**Use descriptive folder names.** For multi-module repositories, clear folder names help users understand what each module contains at a glance.
