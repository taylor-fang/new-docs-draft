---

title: VM image
description: Reference for the sandbox environment Locadex uses to run workflows.

---

# VM image

Locadex runs workflows in a sandboxed environment.

The sandbox installs dependencies, runs configured commands, updates files, and prepares pull request changes.

## Environment variables

Environment variables configured in **Locadex > Configuration > Secrets** are injected into the sandbox when workflows run.

Use them for API keys, tokens, or command configuration.

## Commands

Pre-process and post-process commands run in the sandbox.

Commands run from the repository root.

For monorepos, configure **App Root Directory** and make sure commands target the correct app.

## Package manager

The selected package manager is used to install dependencies in the sandbox.

Set it from **Locadex > Configuration > General**.

## Details to confirm

The exact VM image details should be confirmed before publishing this reference page.

Confirm:

- Operating system.
- Preinstalled language runtimes.
- Preinstalled package managers.
- Network access rules.
- File system limits.
- Workflow timeout limits.
- Cache behavior.