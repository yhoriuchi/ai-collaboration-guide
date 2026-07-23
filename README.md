# Guide to Recording AI Use

This repository provides a practical, tool-agnostic convention that helps researchers automatically record substantive AI use.

The central idea is simple: install persistent instructions that tell a file-capable AI assistant to maintain a dated, human-readable project-history file alongside the work. The record should say what the researcher requested, what the tool did, what files or evidence it used, what changed, and how the result was verified. Individual researchers and teams in any discipline may use the convention with manuscripts, data, code, literature reviews, presentations, grants, teaching materials, or other research work.

The main worked example now follows the architecture in the [Replication Package Guide](https://yhoriuchi.github.io/replication-package-guide/): one approved common research-project root, separate manuscript and analysis repositories, and exactly one active `project_history/` at the common root. The manuscript repository may connect to Overleaf. The same convention works with Codex, Claude Code, and other file-capable AI assistants.

It provides:

- Reusable instructions that can be adapted to different AI tools.
- Ready-to-use setup prompts for Codex and Claude Code.
- A `project_history` convention that AI tools should maintain automatically.
- Guidance for common-root, two-repository, Overleaf-connected, and simpler single-project workflows.
- A general default for research projects that do not already have a history convention.

## Quick Start

### Worked example: one common project root

1. Create or identify the common parent containing root `AGENTS.md`, root `README.md`, `manuscript/`, `analysis/`, one `project_history/`, and optional `others/`.
2. Open `docs/codex-setup.md`, copy the setup prompt, and paste it into Codex. Codex should install the global instructions automatically while preserving and merging with any existing user instructions in `~/.codex/AGENTS.md`.
3. Open the common parent as the single Codex or Claude workspace so the agent can inspect both repositories.
4. Prompt normally. Codex should automatically create or append to `project_history/Your_Name/YYYY-MM-DD by Codex.md` after substantive work.

Do not create separate active histories inside `manuscript/`, `analysis/`, an Overleaf mirror, the public replication package, or `others/`. If a single repository or Overleaf folder is the entire project, use that established root.

Users should not need to name the model or reasoning setting in each prompt. The AI agent should record those settings automatically from available task/runtime metadata or the visible interface. If the environment genuinely does not expose a setting, the history should identify only that field as unavailable rather than asking the user routinely or guessing.

Each daily history uses the actual tool name:

```text
project_history/Your_Name/YYYY-MM-DD by Codex.md
project_history/Your_Name/YYYY-MM-DD by Claude.md
```

Each substantive entry records the exact model display name, family, slug, reasoning label and raw value, speed mode, and service tier when those fields are exposed. For multi-repository or replication work, it also records the common root, both repositories' Git states, journal requirements, external sources and access dates, affected files, concrete verification evidence, and remaining risks.

Project history is private by default. Keep it outside the public replication package, manuscript repository, and journal submission unless the project explicitly requires it there.

### Other tools and workflows

Claude Code users can follow the equally supported `docs/claude-setup.md` instructions. Use the same recording principle with another AI assistant, approved cloud storage, a local repository, or direct/GitHub-connected Overleaf. Adapt the instruction-file location while preserving one authoritative project history and the auditability of the record.

Automatic recording requires an AI assistant that can write project files and follow persistent instructions. If a tool cannot do that, export or copy a concise activity record manually. In all cases, follow applicable privacy, confidentiality, ethics, authorship, disclosure, institutional, funder, journal, and repository requirements.

For replication-package work, read the current Replication Package Guide, the root project instructions and map, and the target journal's current official requirements before substantive work. Journal instructions control package requirements; this guide and the root project instructions control AI-use recording and project-history location.
