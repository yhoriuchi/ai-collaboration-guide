# Claude Code Setup

This is meant to be easy. Collaborators can keep writing and revising in Overleaf as usual. The only Claude setup is to install the shared instructions and choose the existing Overleaf project folder as the Claude Code working directory.

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

In Claude Code, create/open a project and choose the existing Overleaf project folder as the working directory:

```text
~/Dropbox/Apps/Overleaf/Project-Name
```

Do not reorganize Dropbox folders. The folder only matters because Claude needs a project directory.

After that, prompt Claude in whatever way is natural for the task. A useful first message is:

```text
This Claude Code project uses the existing Overleaf project folder as its working directory.
Please follow the shared CLAUDE/AGENTS instructions and save the project_history log automatically.
```

You do not need to manually create the history log each time. The shared instructions ask Claude to create or append it automatically.

## Reference

Claude Code memory docs:

https://code.claude.com/docs/en/memory
