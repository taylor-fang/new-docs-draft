# GT Docs Draft

This repository is a draft workspace for the new General Translation documentation. It is intended for review, collaboration, and automated content migration before these docs are moved into the production docs repository.

## Ready for Review

Platform and sections (Dashboard, Locadex, OpenAPI, and Core) are completed and ready for review: 

- `Platform/platform-filetree.json` defines the full proposed Platform docs navigation tree.
- `Platform/Dashboard`, `Platform/Locadex`, `Platform/OpenAPI`, and `Platform/Core` contain draft markdown pages and section indexes.
- `Platform/Core/Reference/paths-and-headers.json` and `Platform/OpenAPI/paths-and-headers.json` describe the reference page groups, page titles, target paths, and descriptions used to populate the reference sections.

## In Progress

Still to be completed: CLI, React, Node, Python, Integrations, and Overview pages (Get Started, Key Terms and Concepts, Use Agents)

## Path Conventions

All docs paths in JSON are lowercase. `Platform/platform-filetree.json` uses full docs paths:

```text
/docs/platform/...
```

The reference manifests use repository-relative paths:

```text
core/reference/...
openapi/reference/...
```

## Review Checklist

Checks:

- Convert to mdx and update links
- Check correct `path` formatting and no broken links

## Notes/To-dos

- Add an edit in Github button on every page
- Link OpenAPI yaml file (add button and link in text on OpenAPI Get Started page)
- Change Supported Locales page in Dashboard section to a machine-readable list
- Add a header component for "Related pages" (mirroring Next.JS docs) that automatically links those pages at the end of each page
- Agent/linter checks:
  - Check and note when features are gated to Enterprise customers
  - Add screenshots of relevant pages in the Dashboard section and keep them updated if the Dashboard changes

