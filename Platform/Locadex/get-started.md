---

title: Get started with Locadex  
description: Learn how to use Locadex, the AI agent which connects your codebase, translations, and content sources. It’s the fastest way to run General Translation's full-stack localization.

---

# Get started with Locadex

Locadex is the General Translation AI agent that connects your codebase, translations, and content sources. 

It takes **5 minutes** to set up, after which your Project will be configured and translated into any language you choose **automatically**. Locadex is built to handle 100% of internationalization (i18n) and translation work for you.

Locadex currently supports **Next.js** and **Mintlify** Projects only.

## How Locadex works

Locadex works inside your GitHub repository and automatically opens PRs for every generated change. Three workflows keep all of your translations up to date:

- **Codegen** wraps source code with the right internationalization (i18n) library calls, such as `t()` and the `T` component.
- **Translation** translates source content into every target language and updates translation files.
- **Update Locales** updates Project files when languages are added or removed.

Each workflow can run manually, on pull requests, or on Commits. You choose the trigger settings.

## Quickstart

Setting up Locadex takes just 5 minutes. You will need a [General Translation](https://dash.generaltranslation.com) Project and GitHub repository containing a Mintlify or Next.js App Router project. 

1. **Connect GitHub.** Open your Project from the [Dashboard](https://dash.generaltranslation.com) and go to **Locadex > Agent** in your sidebar. Connect your GitHub account and authorize the connection. Follow the flow, which will guide you through permissions for the repositories you want Locadex to access (all repositories, or a specific selection).
2. **Link your repository.** Back in the Dashboard, select the repository to internationalize. Each Project links to one repository; create additional Projects for additional repositories.
3. **Configure the Project.**
  - **Set app root directory** (for monorepos). Use `.` or leave the field empty when the app is at the repository root.
  - **Optional:** set **package manager** so Locadex can install dependencies in the sandbox and set **linter** so Locadex can preserve code style after changes.
  - **Choose your language(s)**: your source (default) locale and the target languages your application will be translated into. Target languages can be selected from all 120 General Translation supported locales.
4. **Review and merge.** Locadex automatically runs its setup workflow to install the i18n library, configure your Project, and add the translation infrastructure. This may take a few minutes to complete. Open the PR (use **View on GitHub**), review the changes, and merge to complete your setup.

That's it! After the setup PR is merged, Locadex monitors your main branch for commits and updates translations as needed. Review new PRs or **enable [auto-merge](/docs/platform/locadex/guides/auto-merge)** and your app stays translated without manual work. 

You can trigger a run yourself at any time with **Run Agent**.

## Next steps



### Configuring Locadex

- **Control when Locadex runs:** configure triggers, target branches, generated PR settings, and pre/post-process commands. See [Configure workflows](/docs/platform/locadex/guides/configure-workflows).
- **Merge generated PRs automatically:** enable auto-merge when you want Locadex changes to auto-merge after checks pass. See [Auto-merge Locadex PRs](/docs/platform/locadex/guides/auto-merge).
- **Add secrets for workflow runs:** add environment variables for API keys, tokens, or build settings used in the Locadex sandbox. See [Add environment variables](/docs/platform/locadex/guides/environment-variables).
- **Set up a monorepo:** configure the app root directory when your Mintlify or Next.js app lives in a subdirectory. See [Use Locadex in a monorepo](/docs/platform/locadex/guides/monorepos).



### Managing Locadex translations

- **Inspect workflow runs:** view past workflow runs to debug failures or check status. See [View workflow history](/docs/platform/locadex/guides/workflow-history).
- **Update languages:** change your source locale or target languages. See [Manage languages](/docs/platform/locadex/guides/manage-languages).
- **Review generated translations:** compare locales, make manual edits, and inspect version history. See [Review and edit translations](/docs/platform/dashboard/guides/edit-translations) in the Dashboard.
- **Guide translation quality:** use Context Groups to define glossary terms, product names, and style rules. See [Define translation context](/docs/platform/dashboard/guides/context) in the Dashboard.



### Re-running Locadex setup

- If you need to start the configuration flow again, open **Configuration > General** and click **Re-run setup**. Re-running setup re-detects your framework, locales, and configuration from scratch.

