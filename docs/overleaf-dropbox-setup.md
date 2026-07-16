# Overleaf Dropbox Setup

Use Overleaf Dropbox synchronization so Codex or Claude can use the Overleaf project folder as its working directory.

Collaborators do not need to change how they normally write or revise papers. They can continue using Overleaf directly. The local Dropbox-synced folder is mainly for the AI agent to inspect/edit project files and save `project_history` logs.

## Expected Local Folder

After sync is configured, Overleaf projects should appear under:

```text
~/Dropbox/Apps/Overleaf/
```

Example:

```text
~/Dropbox/Apps/Overleaf/Project-Name
```

Use the synced project folder as the working directory for the Codex or Claude project.

## Important Notes

- Overleaf Dropbox synchronization is a premium feature.
- Each collaborator needs appropriate edit access and an eligible sync setup.
- Dropbox sync does not automatically give every collaborator a local synced copy.
- Avoid renaming or moving synced Overleaf project folders in Dropbox unless you know the sync consequences.
- Collaborators should not manually reorganize local synced files just to use this guide.

## Reference

Overleaf documentation:

https://docs.overleaf.com/integrations-and-add-ons/dropbox
