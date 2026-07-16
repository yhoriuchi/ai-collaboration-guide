# Overleaf AI Setup Guide

This repository is a shareable guide for using AI agents, such as Codex and Claude, with shared Overleaf writing projects.

The setup is intentionally simple. Collaborators should not need to change how they write in Overleaf or manage Dropbox folders.

It provides:

- Global agent instructions for Codex and Claude Code.
- A short setup guide for using an Overleaf project folder as the Codex or Claude working directory.
- A `project_history` convention that AI agents should maintain automatically.

## Quick Start

Collaborators can keep writing and revising papers in Overleaf as usual. I am only asking each collaborator to do a few small setup steps.

1. Enable Overleaf Dropbox integration for the shared project.
2. Install the shared agent instructions by opening `docs/codex-setup.md` or `docs/claude-setup.md`, copying the setup prompt, and pasting it into Codex or Claude. The AI agent should save the global instruction files automatically.
3. In Codex or Claude, create/open a project and choose the existing Overleaf project folder as the working directory.
4. Send instructions to Codex or Claude in whatever way is natural for the task.
5. The AI agent should automatically save logs under `project_history/Your_Name/YYYY-MM-DD by Agent.md`.

That is all. Please do not reorganize Dropbox folders or manually create logs unless something goes wrong.

For details, see `docs/codex-setup.md` or `docs/claude-setup.md`.
