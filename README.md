# Guide to Recording AI Use

This repository provides a practical, tool-agnostic convention that helps anyone automatically record substantive AI use in any project.

The central idea is simple: install persistent instructions that tell a file-capable AI assistant to maintain a dated, human-readable project-history file alongside the work. The record should say what the user requested, what the tool did, what files or evidence it used, what changed, and how the result was verified.

Individuals, teams, organizations, students, researchers, developers, creators, administrators, and others can use the convention for software, websites, business operations, writing, publishing, design, teaching, coursework, research, personal organization, community projects, and other structured work.

It provides:

- Reusable instructions that can be adapted to different AI tools.
- Ready-to-use setup prompts for Codex and Claude Code.
- A `project_history` convention that AI tools should maintain automatically.
- Guidance for single-folder, single-repository, multi-repository, cloud-connected, and document-centered workflows.
- A general default for projects that do not already have a history convention.

## Quick Start

### One project root

1. Create or identify the highest practical folder representing the intended project scope.
2. Open `docs/codex-setup.md`, copy the setup prompt, and paste it into Codex. Codex should install the global instructions automatically while preserving and merging with any existing user instructions in `~/.codex/AGENTS.md`.
3. Open the project root as the AI workspace.
4. Prompt normally. Codex should automatically create or append to `project_history/Your_Name/YYYY-MM-DD by Codex.md` after substantive work.

For a multi-repository project, use the common parent and keep one active history there. Do not create competing histories inside child repositories, mirrors, builds, archives, exports, or deliverable folders.

Users should not need to name the model or reasoning setting in each prompt. The AI agent should record those settings automatically from available task/runtime metadata or the visible interface. If the environment genuinely does not expose a setting, the history should identify only that field as unavailable rather than asking the user routinely or guessing.

Each daily history uses the actual tool name:

```text
project_history/Your_Name/YYYY-MM-DD by Codex.md
project_history/Your_Name/YYYY-MM-DD by Claude.md
```

Each substantive entry records the exact model display name, family, slug, reasoning label and raw value, speed mode, and service tier when those fields are exposed. Adapt the remaining evidence to the project: repositories and deployments, document versions, source assets and exports, datasets and transformations, decisions and approvals, external sources and access dates, concrete verification evidence, and remaining risks.

Project history is private by default. Share or publish it only when the user, organization, or project policy permits it.

### Other tools and workflows

Claude Code users can follow the equally supported `docs/claude-setup.md` instructions. Use the same principle with another AI assistant, approved cloud storage, local folders, repositories, document platforms, or other project systems. Adapt the instruction-file location while preserving one authoritative project history and the auditability of the record.

Automatic recording requires an AI assistant that can write project files and follow persistent instructions. If a tool cannot do that, export or copy a concise activity record manually. In all cases, follow applicable privacy, confidentiality, security, intellectual-property, retention, disclosure, contractual, organizational, platform, and domain-specific requirements.

Research and replication packages remain a supported specialized use case. For replication-package work, the AI agent—not the user—is responsible for reading the current [AI-Assisted Research Project Management and Replication Guide](https://yhoriuchi.github.io/replication-package-guide/), the root project instructions and map, and the target journal's current official requirements before substantive work. The user may read them for context.
