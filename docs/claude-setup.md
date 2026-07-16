# Claude Code Setup

Collaborators can keep writing and revising in Overleaf. The Dropbox-synced Overleaf folder is used as the Claude Code project working directory so Claude can inspect/edit files and save history logs.

Claude Code reads `CLAUDE.md`, not `AGENTS.md`.

## Recommended Setup

Copy the shared `AGENTS.md` file to:

```text
~/.claude/AGENTS.md
```

Then create or edit:

```text
~/.claude/CLAUDE.md
```

Add:

```md
@~/.claude/AGENTS.md
```

This lets Claude Code load the shared instructions without duplicating them.

## Create or Open a Claude Code Project

In Claude Code, create/open a project and set the working directory to the Dropbox-synced Overleaf project folder:

```text
~/Dropbox/Apps/Overleaf/Project-Name
```

After that, prompt Claude in whatever way is natural for the task. A useful first message is:

```text
This Claude Code project uses the Dropbox-synced Overleaf folder as its working directory.
Please follow the shared CLAUDE/AGENTS instructions and save the project_history log automatically.
```

You do not need to manually create the history log each time. The shared instructions ask Claude to create or append it.

## Reference

Claude Code memory docs:

https://code.claude.com/docs/en/memory
