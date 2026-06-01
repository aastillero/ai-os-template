# Role Packs

Role packs make this AI OS template portable across different jobs.

The active role is copied into:

```text
context/role-profile.md
```

Reusable role definitions live here:

```text
roles/<role-name>/profile.md
```

## Current role pack

```text
roles/delivery-lead/profile.md
```

## Creating a new role pack

1. Copy `roles/_template/profile.md`.
2. Rename the folder to the role name, using lowercase hyphens.
3. Fill in the role profile.
4. Copy that profile into `context/role-profile.md` when creating a role-specific edition.
5. Adjust cadence prompts, project/workstream templates, and future skills only where needed.

Examples:

```text
roles/product-owner/profile.md
roles/engineering-manager/profile.md
roles/qa-lead/profile.md
roles/business-analyst/profile.md
```
