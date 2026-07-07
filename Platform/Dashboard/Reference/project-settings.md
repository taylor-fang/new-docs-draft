# Project settings

Project settings control how an individual project appears and how its translations are delivered.

## General settings

- Update the project **display name**. This changes how the project appears in the dashboard.
- Update the project **source locale**. This changes the language your content is authored in, but does not update existing translations.
- Enable the **CDN setting** to serve translations from a global CDN for faster load times.
- Enable **AI Context**, which uses contextual information to improve AI translation quality

## Project ID

The project ID is read-only and can be copied from Settings. 

Use it in SDK, CLI, and CI configuration when a workflow needs to target a specific project.

```bash
GT_PROJECT_ID=...
```

## Danger zone

Permanently delete a project, all its translations, API keys, and data. This cannot be undone.