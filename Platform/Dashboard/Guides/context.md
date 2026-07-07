---

title: Guide translations with context and key terms

description: Use Context Groups with Glossary (key terms) and Directives (tone and style) to guide AI translation.

---

# Guide translations with context and key terms

Define how your product should be translated, including **terminology and style** that should stay consistent across projects and across your whole organization. 

General Translation applies shared context through **Context Groups**, which include a **Glossary** (key terms) and **Directives** (tone and style). Context Groups are applied to new translations, but do not automatically update existing translations. See Apply Glossary.

## Basic translation context workflow

1. Open your Organization in the Dashboard.
2. Go to the **Context** page.
3. Create a **Context Group**.
4. Add a **Glossary** (for terminology) and/or **Directives** (for style).
5. **Assign** your Context Group to relevant project(s).
6. Translate, regenerate translations, or apply Glossary updates.

## What are Context Groups?

Context Groups are reusable collections of translation context. They combine Glossary terms and Directives so you can guide translations consistently across your organization.

a) **Glossary** defines **terminology**: product and brand names, features, and technical terms. *Example: Locadex is the GT agent which should not be translated*

b) **Directives** define **style**: tone, audience, formality, conventions, and formatting. *Example: Use active voice, avoid jargon, use formal “sie”*

All Context Groups are stored at the Organization level, and can be assigned to one or more Projects.

## Create and assign Context Groups

You can create a Context Group from the organization or from a project.

### Create a Context Group for multiple projects

Use the organization-level flow when you want to create a shared group first, then assign it to one or more projects.

1. Open **Context** in the organization sidebar.
2. Click the plus sign and **Create new group**.
3. Enter name and confirm.
4. Add relevant **Glossary** terms and **Directives**.
5. Open each relevant project.
6. Assign the group from the project's **Context** tab.

Assigned context groups apply their glossary terms and directives whenever the project is translated, regenerated, or processed by Locadex.

### Create a Context Group for the current project

Use the project-level flow when you are already working in a project and want the group assigned there immediately.

1. Open **Context** in the project sidebar.
2. Click the plus sign and **Create new group**.
3. Enter name and confirm. Select the checkbox to **Autogenerate context** from your project files.
4. Add relevant **Glossary** terms and **Directives**.

When you create a context group from a project, it is still created at the organization level. We automatically assign it to the current project. 

### Import existing Context Group

Move context between tools or seed a group from an existing terminology list. **Export** to download a group's glossary and directives. **Import** to fill an empty Glossary and Directive fields from a supported file.

## Add key terms in Glossary

Use the glossary for words and phrases that need consistent treatment across translations. Glossary terms are useful for:

- Brand names
- Product names
- Feature names
- Technical terms
- Phrases that should stay untranslated

Add terms to the context group that should own them. If a term appears in multiple assigned groups, the higher-priority group wins.

## Add tone and style in Directives

Use directives for translation instructions that are broader than a single term. Directives are useful for:

- Tone
- Target audience
- Formal or informal address
- Locale-specific style rules
- Product or domain-specific instructions

Directives can be global or locale-specific. Use locale-specific directives when guidance should apply only to one target language or region.

## Set context priority

When a project has multiple assigned groups, priority determines which guidance wins when groups overlap.

- The top group has the highest priority
- Reorder groups from the project Context page
- If the same glossary term appears in multiple groups, the higher-priority group is used
- Newly generated or imported terms are saved to the highest-priority group



## Apply context to existing translations

Context Groups are applied whenever the AI generates translations, including initial translation, regenerating translations, and Locadex processing.

However, editing Context Groups does not automatically rewrite every existing translation. To apply your changes:

- Use the CLI when you want AI to create new versions of every file.
- Use **Apply Glossary** when you only need existing translations to pick up selected Glossary terms.



### Apply Glossary

Apply Glossary retranslates only files that contain selected Glossary terms.

1. Open the Project **Context** page.
2. Select the Glossary terms you want to apply.
3. Click **Apply** and choose the locales to update.
4. Start the Apply job, and wait for the background job to finish.
5. Review the updated translations.

