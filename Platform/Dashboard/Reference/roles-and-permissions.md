---

title: Roles and permissions
description: Understand the default organization roles, permission categories, and how permissions inherit across enterprises, organizations, and projects.

---

# Roles and permissions

Roles control what members can see and do across your organization and projects.

## Organization roles

When an organization is created, four default roles are set up automatically:

| Role          | Description                                                                                                           |
| ------------- | --------------------------------------------------------------------------------------------------------------------- |
| **Admin**     | Full access to all organization and project settings, members, billing, and translations. Can delete the organization. |
| **Developer** | Technical access to projects—API keys, GitHub integration, Locadex, and usage data. Cannot manage members or billing. |
| **Editor**    | Can read, edit, and review translations. No access to settings, members, or billing.                                  |
| **Member**    | Can view the organization but has no specific permissions. Useful as a base role with additional per-user overrides.  |

## Enterprise roles

Enterprise accounts have an additional layer of roles for managing multiple organizations. For details on enterprise roles and permissions, [contact us](https://generaltranslation.com/en-US/enterprise/contact).

## Permissions reference

Permissions are grouped into categories. The table below shows which default roles have access to each permission.

### Organization permissions

| Permission               | Admin | Developer | Editor | Member |
| ------------------------ | :---: | :-------: | :----: | :----: |
| Update org settings      |   ✓   |           |        |        |
| Manage projects & plan   |   ✓   |           |        |        |
| Manage members           |   ✓   |           |        |        |
| View usage               |   ✓   |     ✓     |        |        |
| Read GitHub integration  |   ✓   |     ✓     |        |        |
| Write GitHub integration |   ✓   |     ✓     |        |        |

### Project permissions

| Permission               | Admin | Developer | Editor | Member |
| ------------------------ | :---: | :-------: | :----: | :----: |
| Update project settings  |   ✓   |           |        |        |
| Read API keys            |   ✓   |     ✓     |        |        |
| Create & delete API keys |   ✓   |     ✓     |        |        |
| Read project context     |   ✓   |           |        |        |
| Write project context    |   ✓   |           |        |        |
| Read Locadex settings    |   ✓   |     ✓     |        |        |
| Write Locadex settings   |   ✓   |     ✓     |        |        |

### Translation permissions

| Permission                    | Admin | Developer | Editor | Member |
| ----------------------------- | :---: | :-------: | :----: | :----: |
| Read translations             |   ✓   |           |   ✓    |        |
| Edit translations             |   ✓   |           |   ✓    |        |
| Review & approve translations |   ✓   |           |   ✓    |        |

### Roles & billing permissions

| Permission              | Admin | Developer | Editor | Member |
| ----------------------- | :---: | :-------: | :----: | :----: |
| View roles              |   ✓   |           |        |        |
| Create & delete roles   |   ✓   |           |        |        |
| Assign roles to members |   ✓   |           |        |        |
| View billing            |   ✓   |           |        |        |
| Update billing          |   ✓   |           |        |        |

## Permission inheritance

Permissions flow downward through the hierarchy:

**Enterprise → Organization → Project**

If a user has a permission at the enterprise level, they automatically have it for all organizations and projects within that enterprise. Similarly, organization-level permissions apply to all projects in that organization.