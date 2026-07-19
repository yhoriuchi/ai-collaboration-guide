# Guide to Recording AI Use

This repository provides a practical, tool-agnostic convention that helps researchers automatically record substantive AI use.

The central idea is simple: install persistent instructions that tell a file-capable AI assistant to maintain a dated, human-readable project-history file alongside the work. The record should say what the researcher requested, what the tool did, what files or evidence it used, what changed, and how the result was verified. Individual researchers and teams in any discipline may use the convention with manuscripts, data, code, literature reviews, presentations, grants, teaching materials, or other research work.

The main worked example uses the author's own **Dropbox + Overleaf + Codex** workflow because it lets collaborators continue writing in Overleaf while Codex works on the synchronized local project folder and records its work automatically. The same convention works with Claude Code and other file-capable AI assistants; the example is not a universal product recommendation.

It provides:

- Reusable instructions that can be adapted to different AI tools.
- Ready-to-use setup prompts for Codex and Claude Code.
- A `project_history` convention that AI tools should maintain automatically.
- Guidance for Dropbox + Overleaf and GitHub-centered projects.
- A general default for research projects that do not already have a history convention.

## Quick Start

### Worked example: Dropbox + Overleaf + Codex

1. Enable Overleaf Dropbox integration for the shared project.
2. Open `docs/codex-setup.md`, copy the setup prompt, and paste it into Codex. Codex should install the global instructions automatically.
3. In Codex, open the synchronized Overleaf project folder as the working directory.
4. Prompt Codex normally. It should automatically create or append to `project_history/Your_Name/YYYY-MM-DD by Codex.md` after substantive work.

### Other tools and workflows

Claude Code users can follow the equally supported `docs/claude-setup.md` instructions. Use the same recording principle with another AI assistant, a different synchronized folder, a local repository, or a GitHub-centered Overleaf project. Adapt the instruction-file location and working-directory convention to the tool while preserving the content and auditability of the history record.

Automatic recording requires an AI assistant that can write project files and follow persistent instructions. If a tool cannot do that, export or copy a concise activity record manually. In all cases, follow applicable privacy, confidentiality, ethics, authorship, disclosure, institutional, funder, journal, and repository requirements.
