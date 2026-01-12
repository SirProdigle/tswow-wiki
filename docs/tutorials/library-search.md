---
layout: default
title: Library Search
nav_order: 5
---

# TSWoW Library Search

The TSWoW Library Search is a tool for discovering community-created modules and libraries.

## [**Browse Libraries**](https://tswow-library-search.bold-term-1c95.workers.dev/)

## Making Your Module Discoverable

To have your module listed in the library search, you need to tag your GitHub repository and follow a few structural conventions.

### GitHub Topic

Add the `tswow-module` topic to your GitHub repository. This is how the library search discovers modules:

1. Go to your repository on GitHub
2. Click the gear icon next to "About" in the right sidebar
3. Add `tswow-module` to the Topics field
4. Save changes

Your repository will be indexed automatically within a few hours.

### Repository Structure

The library search supports two repository structures:

#### Single Module Repository

If your repository contains a single module, place the `datascripts/` or `livescripts/` folder at the repository root:

```
myname-mymodule/
├── datascripts/
├── livescripts/
├── assets/
└── README.md
```

#### Multi-Module Repository

If your repository contains multiple modules, each top-level folder (that isn't an excluded name) is treated as a separate module:

```
module-library/
├── myname-module-one/
│   ├── datascripts/
│   └── README.md
├── myname-module-two/
│   ├── datascripts/
│   └── README.md
└── README.md
```

**Note:** Certain common directory names are excluded from module detection: `.github`, `node_modules`, `docs`, `tests`, `src`, `lib`, `examples`, and similar development/tooling directories.

### README Files

Include README files to help users understand your modules:

- **Repository README.md** - Explain the purpose of your repository, installation instructions, and an overview of what modules are included.
- **Per-module README.md** - For multi-module repositories, include a README.md in each module folder explaining what that specific module does.

README content is indexed for search, so descriptive documentation helps users find your modules.

## How Search Works

The library search uses semantic vector indexing to help users find relevant modules. It understands the meaning behind your query.

### What Gets Indexed

The following content from your repository is indexed and used for search matching:

- Repository name
- Repository description (from GitHub's "About" section)
- GitHub topics
- README content (first ~5,000 characters)

### Tips for Better Discoverability

- Write a clear, descriptive repository description in GitHub's "About" section
- Add relevant GitHub topics beyond just `tswow-module` (e.g., `custom-class`, `profession`, `dungeon`)
- Include keywords and use cases in your README that describe what your module does
- Use descriptive module folder names in multi-module repositories
