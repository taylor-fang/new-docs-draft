---

title: API keys
description: Create and manage project and organization API keys for apps, local development, and automation.

---

# API keys

API keys authenticate your apps, CLI, and automation with General Translation. Use the narrowest key scope that fits the workflow.

## Key scopes

GT supports two API key scopes:

- **Organization keys** for organization-level automation. Use them for org-level automation or workflows that need to operate across projects in the organization.
- **Project keys** for a single project. Use them for deployed apps, local development, previews, and project-scoped tooling.

Organization keys and project keys have different creation flows. Project keys are created as production or development keys. Organization keys use a permission selector.

## Create Organization keys

Create organization keys from **Organization -> API Keys**. Organization keys use the `gtx-org-` prefix and can be configured with a custom permission set. 

Permissions are configured per resource. `Write` includes `Read`.

| Resource                | Read                                  | Write or enabled                                      |
| ----------------------- | ------------------------------------- | ----------------------------------------------------- |
| **Files**               | Read project files and translations   | Upload source content and write translated files      |
| **Context**             | Read project and organization context | Manage context groups, glossary, and directives       |
| **Runtime translation** | Not applicable                        | Translate content on demand                           |
| **Translation queue**   | Not applicable                        | Queue file translation jobs for background processing |
| **Project settings**    | Not applicable                        | Update project settings such as the default locale    |

Grant each key only the permissions it needs.

## Create Project keys

Create project keys from **Project -> API Keys**. Copy the full key immediately and store it in environment variables, a secrets manager, or another secure store.

- **Production keys** start with `gtx-api-`.
  - Use them in deployed applications and production automation. Production translations use published content.
- **Development keys** start with `gtx-dev-`.
  - Use them for local development, preview environments, and test automation. Development keys let you test translations before they are published, without affecting your live application.
  - Do not use development keys in production.

In most SDK and CLI workflows, use the key with your project ID:

```bash
GT_API_KEY=gtx-api-...
GT_PROJECT_ID=...
```
## Manage keys

Use descriptive names so keys are easy to identify later. 

Open the key list for the project or organization to review existing keys. The key list shows:

- **Preview**, a truncated version of the key for identification
- **Created At**, when the key was generated
- **Last Used**, when the key was last used
- **Delete**, to revoke a key you no longer need

Revoke keys that are no longer used, and create replacements when rotating credentials.

## Security practices

- Never commit keys to source control
- Store keys in environment variables or a secrets manager
- Use separate keys for development, staging, and production
- Rotate keys periodically 
- Revoke unused keys
- Prefer the narrowest scope that works for the integration

