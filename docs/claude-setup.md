# Claude Code Setup

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

## Start a Task

Open the Dropbox-synced Overleaf project folder:

```text
~/Dropbox/Apps/Overleaf/Project-Name
```

Then prompt Claude Code:

```text
We are working in an Overleaf project synced through Dropbox.
Follow the global CLAUDE/AGENTS instructions.
Save today's project history under project_history/Your_Name/YYYY-MM-DD by Claude.md.
Record model, reasoning effort, speed/service tier, files changed, commands run, and verification.
```

## Reference

Claude Code memory docs:

https://code.claude.com/docs/en/memory
