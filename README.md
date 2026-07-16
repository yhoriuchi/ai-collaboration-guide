# AI Collaboration Guide

This repository is a shareable guide for using AI agents, such as Codex and Claude, with shared Overleaf projects and research software projects.

It provides:

- Global agent instructions for Codex and Claude Code.
- A collaborator-facing setup guide for Overleaf Dropbox sync.
- A `project_history` convention for documenting AI-assisted work.
- Templates that collaborators can copy into their own projects.
- A simple static website entry point in `index.html`.

## Quick Start

1. Open the website home page: `index.html`.
2. Read `docs/overleaf-dropbox-setup.md`.
3. Install the global agent instructions:
   - Codex: copy `AGENTS.md` to `~/.codex/AGENTS.md`.
   - Claude Code: copy `AGENTS.md` to `~/.claude/AGENTS.md`, then copy `CLAUDE.md` to `~/.claude/CLAUDE.md`.
4. Work from the local Dropbox-synced Overleaf project folder.
5. Save AI work logs under `project_history/Your_Name/YYYY-MM-DD by Agent.md`.

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
