---

name: Internal skill
description: Style guide for writing and updating General Translation Platform docs (the Platform/ folder covering Dashboard, Locadex, OpenAPI, and Core). Use when creating, editing, reviewing, or restructuring any Markdown page, index.md, frontmatter, or filetree entry under Platform/, or when the user asks about docs voice, structure, naming, or formatting conventions.

---

# Platform docs style guide

Rules for authoring and updating docs under `Platform/`. Follow these to preserve the existing style, structure, and flow. The agent already knows Markdown; this captures only project-specific conventions.

## Information architecture

Every product (Dashboard, Locadex, OpenAPI, Core) follows the same three-section spine:

- **Get Started** — how the product/section is organized and where to start.
- **Guides** — one page per task; self-contained how-tos.
- **Reference** — fact/lookup pages, optionally grouped into subsections.

Structure: **Product > Section > Pages** (Reference pages may have **subsections**).

### Get Started

- Usually a single condensed page (`get-started.md`).
- Split into **Overview** + **Quickstart** *only* when the section needs more explanation of what it does before a reader can start (as with the Core library). Otherwise keep it to one page.



### index.md rules

- Get Started, Guides, and Reference each get an `index.md` that only points to what is accessible in that section.
- **Reference subsections do not get an** `index.md`**.** Instead, the parent Reference index links to the **first page** of each subsection, with the description "Browse [Product] [Subsection] pages."



## File and folder naming

- File names: condensed to **3 words or fewer, ideally 2 or fewer**, lowercase, hyphenated (`edit-translations.md`, `configure-workflows.md`, `vm-image.md`).
- Name by topic, not verb phrase (`monorepos.md`, `annotations.md`).
- Avoid spaces in folder names (use `get-started/`, not `Get Started/`) so URLs do not need `%20` encoding.



## Frontmatter

Use this exact structure (blank line after the opening `---`, blank line before the closing `---`):

```text
---

title: Add annotations
description: Use labels, notes, and comments to coordinate translation review by entry and locale.

---
```

- `title`: **sentence case** — capitalize only the first word, except proper/product names (Dashboard, Locadex, Core, Organization, Project, Enterprise, Context Group, Glossary, Directives, GitHub). No trailing spaces. The `title` must match the page H1 exactly.
- `description`: one sentence ending with a period, action-oriented ("Configure…", "Review…", "Learn…").
- **API/library reference pages** add a second sentence: `API reference for [function/method/type].` Apply this to all reference pages, including OpenAPI endpoints. *Example: "…into a target locale. API reference for translate."*



## Page structure

1. **H1** right after the frontmatter, matching the title in sentence case.
2. **Intro**: 1–3 short sentences with no heading, stating what the page is and when to use it. Optionally one more short line for constraints or scope.
3. **Sections** as `##`.



### Index page

H1 = section name; one line repeating the section description ("Browse how-to Guides for…" / "Browse Reference pages for…"); then a bullet list of links:

```text
- [Add annotations](/docs/platform/dashboard/guides/annotations): Use labels, notes, and comments to coordinate translation review by entry and locale.
```

Link text = destination page title. Format is `[Title](path): description.` (colon, then description ending with a period).

### Get Started page

- Dashboard-style: **Key workflows** → **Configuration** → **Navigation** → **FAQs**.
- Product-heavy start (Locadex): **How [product] works** → **Quickstart** (numbered) → **Next steps** (grouped links).



### Guide page

Intro → optional **Before you start** → a **Basic [x] workflow** numbered list (the happy path) → detailed task sections (`##`). Titles must be understandable and actionable.

### Reference page

Intro → topic sections that enumerate fields/settings/options as bullets (`**Field** is/does …`).

## Lists vs. tables

- **Default to bullet points** for readability and quick scanning.
- **Use a table only when the content is genuinely two-dimensional:**
  - A matrix (roles × permissions with ✓).
  - Comparing items across the same fixed dimensions (annotation types: *Best For* / *Usage*).
  - Reference lookups with parallel columns (locale code / language / script / region / description; API key resource / Read / Write).
- Do not use a table for a simple enumeration or a single description column.



## Numbered vs. bulleted lists

- **Numbered** for ordered procedures (steps that must happen in sequence).
- **Bulleted** for options, sets, and non-ordered enumerations.
- Use the `a)` `b)` `c)` subheading pattern for **parallel sibling alternatives** where the reader picks one path (as in "Create a Context Group" → a) multiple projects, b) current project, c) import/export). Good candidates: alternative setup flows, key scopes, trigger options.



## Voice and formatting

- Address the reader as "you"; use active voice and imperatives.
- **Fragment vs. sentence in lists**: use fragments when simply listing pieces or labels (no period needed); use full sentences (including standalone imperatives like "Revoke unused keys.") when describing steps or actions, and end those with a period. Be consistent within a single list. List items that complete a lead-in stem ("From the page, you can:") are fragments and take no period.
- **Italicize notes and examples**: `*Note: …`* and `*Example: …*`.
- **Bold** UI elements the user interacts with: buttons, page names, fields, toggles (**Save**, **Translate**, **App Root Directory**).
- **Inline code** for code identifiers, file names, locale codes, environment variables, key prefixes, and headers (`en-US`, `GT_API_KEY`, `gtx-api-`, `x-gt-api-key`).



### Canonical term casing

Always capitalize as product terms: **Organization**, **Project**, **Enterprise** (product scopes), **Context Group**, **Glossary**, **Directives**, **Locadex**, **Dashboard**, **Core**, **GitHub**. Lowercase "group", "term", and "directive" only when not part of the proper term.

Capitalize the scope noun even inside hyphenated compounds (Organization-level, Project-wide, Project-scoped, Project-specific). Keep it lowercase only inside code, URLs, permission strings (`project:files:read`), headers (`x-gt-project-id`), and identifiers (`projectId`, `GT_PROJECT_ID`).

### Referring to Dashboard locations

Use a bolded breadcrumb with `>`: **Locadex > Configuration > General**, **Project > Context**. Standardize on `>` (never `->`).

## Links

- Internal links use root-relative `/docs/platform/...` paths.
- **Omit the** `.md` **suffix in all Markdown links** (body prose and index link lists). Note that JSON `path` fields in `platform-filetree.json` and `paths-and-headers.json` keep `.md`, since those are structural file locations.
- Link punctuation goes **outside** the brackets: `[Annotations](…).`, not `[Annotations.](…)`.
- Do not wrap a Markdown link in backticks (``[GT](…)`` renders literally). Use either code (`GT`) or a link ([GT](…)), not both.



## Code blocks

- Fence with a language (`bash`, `typescript`, `json`, `txt`).
- Use `title="src/index.ts"` for file snippets and `title="Output"` for response examples.
- Keep runnable examples minimal and consistent (e.g. `gt.translate('Hello, world!', 'es')`).



## Consistency checks before finishing

- Navigation separators use `>`, not `->`.
- `.md` link suffix usage is consistent within the file.
- Notes and examples are italicized.
- Organization/Project/Context Group casing matches the canonical terms.
- API reference descriptions end with the `API reference for X.` sentence.
- No broken internal links (verify the target file exists).
- No typos; sentences end with periods.

