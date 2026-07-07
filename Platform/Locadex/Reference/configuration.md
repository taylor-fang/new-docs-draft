---

title: Configuration
description: Reference for Locadex general settings, workflows, languages, secrets, and danger zone actions.

---

# Configuration

Use **Locadex > Configuration** to control how Locadex runs in your repository.

## General

General settings apply to the Locadex agent for the Project.

- **App Root Directory** is the path to your app. Use this for monorepos.
- **Package Manager** is used to install dependencies in the sandbox.
- **Linter** runs after changes to preserve code style.
- **Email Reminders** sends reminders about open pull requests after a selected delay.
- **Framework** is detected during setup.

Email reminder options are:

- 6 hours
- 12 hours
- 1 day
- 2 days
- 1 week
- 2 weeks

Supported frameworks are currently:

- Mintlify
- Next.js

## Codegen

Codegen configures how Locadex wraps source code with internationalization library calls.

Settings include:

- Enabled or disabled.
- Trigger.
- Target Branch.
- Branch Prefix.
- Auto-merge PRs.
- Run on exact content changes.
- Save local edits.
- Pre-process Command.
- Post-process Command.
- Custom PR Title.
- Custom Commit Message.

## Translation

Translation configures how Locadex translates source content into target languages and updates translation files.

Settings include the same workflow controls as Codegen.

## Locales

Locales configures how Locadex updates files when languages are added or removed.

Settings include the same workflow controls as Codegen and Translation.

## Secrets

Secrets are environment variables injected into the sandbox when Locadex runs workflows.

Each variable has:

- Key
- Value

Use secrets for API keys, tokens, or pre-process and post-process configuration.

## Trigger options

Workflow trigger options are:

- **Manual only**
- **On pull request**
- **On commit**

## Danger Zone

Danger Zone actions affect the Locadex integration for the Project.

- **Disable monitoring** stops automatic workflow triggering. Settings and history are preserved.
- **Re-run setup** re-detects framework, locales, and configuration from scratch.
- **Disconnect repository** removes the link between the Project and the GitHub repository. Workflow history and settings are preserved.