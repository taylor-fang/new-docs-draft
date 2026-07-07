---

title: Agent page
description: Reference for the Locadex Agent page, repository status, languages, and recent workflow runs.

---

# Agent page

The Agent page is the main status page for Locadex.

Open it from **Locadex > Agent** in the project sidebar.

## Repository

The repository header shows:

- Repository name.
- GitHub owner and repository path.
- Repository visibility.
- Current monitoring state.
- App root directory when configured.

Use **View on GitHub** to open the connected repository.

Use **Run Agent** to start Locadex manually.

## Status

The status area shows whether Locadex is monitoring the repository.

When Locadex is monitoring, it watches the repository and processes new changes according to workflow triggers.

## Languages

The Languages section shows:

- Source locale.
- Target languages.

Click **Edit** to change languages.

Saving language changes creates a pull request to update locale configuration in the repository.

## Recent workflow runs

The Agent page shows the most recent workflow runs.

Click **View all** to open the History page.