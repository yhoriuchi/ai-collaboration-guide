# AI Collaboration Guide

This repository is a shareable guide for using AI agents, such as Codex and Claude, with shared Overleaf projects and research software projects.

It provides:

- Global agent instructions for Codex and Claude Code.
- A short setup guide for using an Overleaf project folder as the Codex or Claude working directory.
- A `project_history` convention that AI agents should maintain automatically.
- Templates that collaborators can copy into their own projects.
- A simple static website entry point in `index.html`.

## Quick Start

Collaborators can keep writing and revising papers in Overleaf as usual. The local Dropbox-synced folder is mainly the working directory for Codex or Claude.

1. Install the shared agent instructions:
   - Codex: copy `AGENTS.md` to `~/.codex/AGENTS.md`.
   - Claude Code: copy `AGENTS.md` to `~/.claude/AGENTS.md`, then copy `CLAUDE.md` to `~/.claude/CLAUDE.md`.
2. In Codex or Claude, create/open a project and set the working directory to the Dropbox-synced Overleaf project folder.
3. Send instructions to Codex or Claude in whatever way is natural for the task.
4. The AI agent should save logs under `project_history/Your_Name/YYYY-MM-DD by Agent.md`.

For details, see `docs/codex-setup.md` or `docs/claude-setup.md`.

## Repository Layout

```text
.
├── README.md
├── AGENTS.md
├── CLAUDE.md
├── index.html
├── styles.css
└── docs/
    ├── claude-setup.md
    ├── codex-setup.md
    ├── overleaf-dropbox-setup.md
    ├── project-history-convention.md
    ├── project-organization.md
    └── examples/
        └── project-history-template.md
```

## Publishing

This folder is ready to become a private GitHub repository. If you want a website, use GitHub Pages and publish from the repository root.

Recommended first setting: keep the repository private and invite collaborators.

## Privacy Notes

Before making this public, remove or generalize:

- Personal names you do not want public.
- Local machine paths.
- Project names not intended for public view.
- Any instructions that reveal private workflows.
