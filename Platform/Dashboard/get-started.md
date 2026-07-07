---

title: Get Started with the Dashboard 
description: Learn how the Dashboard is organized and where to find common translation workflows.

---

# Get started with the Dashboard

The Dashboard is the web app for reviewing translations, guiding the AI with context and glossaries, and managing settings and API keys.

## Common workflows

- **Review and edit translations:** compare locales, make manual edits, and inspect version history. See [Review and edit translations](/docs/platform/dashboard/guides/edit-translations).
- **Define translation context:** use Context Groups to guide terminology and style across projects. See [Define translation context](/docs/platform/dashboard/guides/context).
- **Add annotations:** label entries, add notes, and discuss translation decisions with your team. See [Add annotations](/docs/platform/dashboard/guides/annotations).
- **Create API keys:** use project keys for a single project and organization keys for broader automation. See [API keys](/docs/platform/dashboard/reference/api-keys).
- **Manage team access:** invite members and manage organization settings from the Organization scope. See [Organization Settings](/docs/platform/dashboard/reference/organization-settings) and [Roles and permissions](/docs/platform/dashboard/reference/roles-and-permissions).
- **Configure projects:** update project name, source locale, CDN delivery, AI Context, and project ID from Project settings. See [Project settings](/docs/platform/dashboard/reference/project-settings).
- **Send events to your backend:** use webhooks to receive signed translation events. See [Webhooks](/docs/platform/dashboard/reference/webhooks).
- **Automate the whole process:** see [Locadex](/docs/platform/locadex) to automate localization setup and maintenance.



## Navigation

The dashboard is organized into nested scopes: **Enterprise**, **Organization**, and **Project**. Most teams use Organizations and Projects. Enterprise is a layer for larger teams managing multiple organizations.

- **Enterprise** contains organizations, members, billing, and security settings across multiple organizations.
- **Organization** contains projects, team members, shared context, API keys, and webhooks.
- **Project** contains translations, project context, API keys, settings, and Locadex configuration.

Use the switcher in the header to move between scopes. The sidebar changes based on the selected scope.

If you do not see a page, check that you are in the right organization or project and that your role has access.

## FAQs

**What is General Translation?** General Translation (GT) is a full-stack localization platform that translates your app into any language. It combines i18n libraries, an AI-native translation platform, and Locadex, our purpose-built agent. GT handles localization and internationalization for you end-to-end. By connecting your code, content, and translations, GT builds complete understanding of your codebase and product context. So your translations actually reflect the logic of your application, in native speed and quality.

**How do I get an API key?** Create a project, then open **API Keys** at the project or organization level. Project keys are used for one project. Organization keys support custom permissions for broader automation. See [API keys](/docs/platform/dashboard/reference/api-keys).

**Can I edit translations after they are generated?** Yes. Use the **Translations** page to review and edit generated translations. You can also use annotations to label entries, add notes, and discuss translations with your team. See [Review and edit translations](/docs/platform/dashboard/guides/edit-translations).

**What is context?** Context tells AI how to interpret and translate your product. It helps preserve brand and product names, resolve ambiguous words (like whether "cells" refers to rooms, phones, bacteria, or spreadsheets), and keep style consistent across your organization and projects. GT applies context through Context Groups, which include a Glossary for terminology and Directives for tone and style. See [Define translation context](/docs/platform/dashboard/guides/context).

**How do I share terminology across projects?** Create a Context Group at the Organization level with shared Glossary terms and Directives, then assign it to multiple projects. Changes to the group apply everywhere it is assigned. See [Define translation context](/docs/platform/dashboard/guides/context).

**How do I update existing translations after changing the Glossary?** Select relevant terms and use Apply Glossary to update existing translations that contain selected Glossary terms. See [Define translation context](/docs/platform/dashboard/guides/context).

**How do I regenerate translations?** Use the CLI to run a new translation pass. The Dashboard does not currently support full-file retranslation.

**How do I sync Dashboard edits back to GitHub?** Use Locadex to create pull requests for Dashboard changes, such as manual translation edits or Apply Glossary updates.