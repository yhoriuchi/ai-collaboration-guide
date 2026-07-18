# Guide to Recording AI Use

This repository provides a lightweight, tool-agnostic convention for recording substantive AI use in research and other collaborative projects.

The central idea is simple: ask the AI tool to maintain a dated, human-readable project-history file alongside the work. The record should say what the user requested, what the tool did, what files or evidence it used, what changed, and how the result was verified. Teams may use any storage service, writing platform, version-control system, or AI assistant that fits their workflow.

The preferred example in this guide uses **Dropbox + Overleaf + Codex** because it lets collaborators continue writing in Overleaf while Codex works on the synchronized local project folder and records its work automatically. This is an example, not a requirement.

It provides:

- Reusable instructions that can be adapted to different AI tools.
- Ready-to-use setup prompts for Codex and Claude Code.
- A `project_history` convention that AI tools should maintain automatically.
- Guidance for Dropbox + Overleaf and GitHub-centered projects.

## Quick Start

### Preferred example: Dropbox + Overleaf + Codex

1. Enable Overleaf Dropbox integration for the shared project.
2. Open `docs/codex-setup.md`, copy the setup prompt, and paste it into Codex. Codex should install the global instructions automatically.
3. In Codex, open the synchronized Overleaf project folder as the working directory.
4. Prompt Codex normally. It should automatically create or append to `project_history/Your_Name/YYYY-MM-DD by Codex.md` after substantive work.

### Other tools and workflows

Use the same recording principle with another AI assistant, a different synchronized folder, a local repository, or a GitHub-centered Overleaf project. Adapt the instruction-file location and working-directory convention to the tool, while preserving the content and auditability of the history record. See `docs/claude-setup.md` for one additional implementation.
