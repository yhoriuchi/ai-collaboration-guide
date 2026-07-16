# AI Collaboration Guide

This repository is a shareable guide for using AI agents, such as Codex and Claude, with shared Overleaf projects and research software projects.

The setup is intentionally simple. Collaborators should not need to change how they write in Overleaf or manage Dropbox folders.

It provides:

- Global agent instructions for Codex and Claude Code.
- A short setup guide for using an Overleaf project folder as the Codex or Claude working directory.
- A `project_history` convention that AI agents should maintain automatically.

## Quick Start

Collaborators can keep writing and revising papers in Overleaf as usual. I am only asking each collaborator to do a few small setup steps.

1. Enable Overleaf Dropbox integration for the shared project.
2. Install the shared agent instructions:
   - Codex: copy `AGENTS.md` to `~/.codex/AGENTS.md`.
   - Claude Code: copy `AGENTS.md` to `~/.claude/AGENTS.md`, then copy `CLAUDE.md` to `~/.claude/CLAUDE.md`.
3. In Codex or Claude, create/open a project and choose the existing Overleaf project folder as the working directory.
4. Send instructions to Codex or Claude in whatever way is natural for the task.
5. The AI agent should automatically save logs under `project_history/Your_Name/YYYY-MM-DD by Agent.md`.

That is all. Please do not reorganize Dropbox folders or manually create logs unless something goes wrong.

## Optional First Prompt

After setting up Codex or Claude, you can paste this once at the start of a project:

```text
We are working in a shared Overleaf or research project.
Follow the global AGENTS/CLAUDE instructions.
Treat the current folder as the project root unless told otherwise.
Save today's project history under project_history/Your_Name/YYYY-MM-DD by Agent.md.
Record the exact model, reasoning effort, speed/service tier, files changed, commands run, and verification.
```

For details, see `docs/codex-setup.md` or `docs/claude-setup.md`.
