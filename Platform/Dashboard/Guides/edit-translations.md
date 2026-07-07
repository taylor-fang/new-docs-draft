---

title: Review and edit translations
description: Review generated translations, make manual edits, compare locales, and inspect version history in the Dashboard.

---

# Review and edit translations

Use the Dashboard to review translations and make manual edits. 

To generate a new version of a file instead, see [Regenerate translations](/docs/platform/dashboard/guides/retranslate).

## Basic review workflow

1. Open your Project in the Dashboard.
2. Go to the **Translations** page.
3. Choose **Files** or **Components**.
4. Select or search for the content you want to review.
5. Choose the branch and locale(s).
6. Edit translations inline as needed.
7. Use annotations, history, download, and source visibility tools as needed.

## Browse and find translation content

Select between two views (in the top left):

- **Files** for Markdown, JSON, gettext, and other file-based content.
- **Components** for React and JSX projects where strings live in UI components.

Choose one or more **locales** (in the top right). Use multiple locales to compare translations side-by-side. 

Use **Search** to filter the current view by: 

- File name
- Component name
- Key
- Source text
- Translated text

From any project page, you can also press `⌘K` on macOS or `Ctrl+K` on Windows to search across files and components. Search results link directly to the matching entry.

## Edit translations inline

Click a translation cell to edit it. Edits are drafts until you click **Save.**

Use inline editing when you want to make precise manual changes to the existing translation. 

For supported raw formats, toggle **Raw** to edit the underlying file content in a code editor.

(Note: inline edits update the current translation and do not create a new entry in version history. A new version history entry is created only when source edits are sent for translation.)

## Use file tools to review

File tools help you inspect, compare, and export translated content.

Open **History** to inspect previous translation versions. Use to:

- Compare a manual edit
- Restore a prior state
- Confirm when a translated file chnaged

You can also:

- Download translated output
- Show or hide source content
- Filter by [annotation labels](/docs/platform/dashboard/guides/annotations)

## Track review with annotations

Annotation indicators appear inside each cell: click to open the annotation panel for that entry and locale. Read more about [Annotations.](/docs/platform/dashboard/guides/annotations)