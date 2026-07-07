# GT Docs Draft

This repository is a draft workspace for the new General Translation documentation. It is intended for review, collaboration, and automated content migration before these docs are moved into the production docs repository.

## Ready for Review

Platform and sections (Dashboard, Locadex, OpenAPI, and Core) are completed and ready for review: 

- `Platform/platform-filetree.json` defines the full proposed Platform docs navigation tree.
- `Platform/Dashboard`, `Platform/Locadex`, `Platform/OpenAPI`, and `Platform/Core` contain draft markdown pages and section indexes.
- `Platform/Core/Reference/paths-and-headers.json` and `Platform/OpenAPI/paths-and-headers.json` describe the reference page groups, page titles, target paths, and descriptions used to populate the reference sections.

## In Progress

Still to be completed: CLI, React, Node, Python, Integrations, and Overview pages (Get Started, Key Terms and Concepts, Use Agents)

## Style Guide

`SKILL.md` is the style guide for authoring and updating the Platform docs. It captures the project-specific conventions used throughout `Platform/` — information architecture (Get Started, Guides, Reference), file and folder naming, frontmatter, page structure, lists vs. tables, voice and formatting, canonical term casing, and link rules — plus a consistency checklist to run before finishing edits.

It is also registered as a Cursor Agent Skill (`.cursor/skills/platform-docs/SKILL.md`) so the agent automatically follows these conventions when creating, editing, or reviewing any page under `Platform/`. Update `SKILL.md` whenever a convention changes so the docs and the skill stay in sync.

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

