# Claude Code Setup: Alternative Example

This shows how the same tool-agnostic recording convention can be implemented with Claude Code. Copy the setup prompt below, paste it into Claude Code, and approve the file write if Claude asks. Claude should save the shared global instructions automatically.

## Setup Prompt

```text
Please install the shared instructions for recording AI use in collaborative research projects with Claude Code.

1. Fetch the current AGENTS.md from:
   https://raw.githubusercontent.com/yhoriuchi/ai-collaboration-guide/main/AGENTS.md
2. Create ~/.claude if it does not exist.
3. Save the fetched AGENTS.md content exactly to:
   ~/.claude/AGENTS.md
4. Create or update ~/.claude/CLAUDE.md with exactly this line:
   @~/.claude/AGENTS.md
5. Do not modify any Overleaf project files during this setup.
6. Confirm the final file paths and mention whether any network or file-write permission was needed.
```

## Create or Open a Claude Code Project

Choose the working directory that matches the project's collaboration path:

- **Direct Overleaf:** choose the existing Overleaf project folder:

```text
~/Dropbox/Apps/Overleaf/Project-Name
```

- **GitHub-centered alternative:** choose a local clone of the repository connected to Overleaf. Authors can use their preferred editor, and Claude Code can work through its GitHub access rather than direct Overleaf access.

Do not reorganize Dropbox folders or repository files merely for setup. Before editing in the GitHub-centered workflow, follow the project's branch, commit, review, and synchronization conventions; do not make overlapping unsynchronized edits in GitHub and Overleaf.

After that, prompt Claude in whatever way is natural for the task.

You do not need to manually create the history log each time. The shared instructions ask Claude to create or append it automatically.

If Claude cannot access the URL automatically, open `AGENTS.md` from this repository and ask Claude to save that content to `~/.claude/AGENTS.md` and create or update `~/.claude/CLAUDE.md` with `@~/.claude/AGENTS.md`.

## Reference

Claude Code memory docs:

https://code.claude.com/docs/en/memory
