# Overleaf Dropbox Setup

Most collaborators do not need to worry about Dropbox for this guide.

Collaborators can continue writing and revising in Overleaf directly. The only reason the local folder matters is that Codex or Claude needs an Overleaf project folder as its working directory.

## Expected Local Folder

After sync is configured, Overleaf projects should appear under:

```text
~/Dropbox/Apps/Overleaf/
```

Example:

```text
~/Dropbox/Apps/Overleaf/Project-Name
```

Choose the synced Overleaf project folder as the working directory for the Codex or Claude project.

## Important Notes

- Overleaf Dropbox synchronization is a premium feature.
- Each collaborator needs appropriate edit access and an eligible sync setup.
- Dropbox sync does not automatically give every collaborator a local synced copy.
- Do not rename, move, or reorganize synced Overleaf folders just to use this guide.
- The AI agent should save `project_history` logs automatically.

## Reference

Overleaf documentation:

https://docs.overleaf.com/integrations-and-add-ons/dropbox
