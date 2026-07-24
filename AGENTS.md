# Global Agent Instructions for Recording AI Use in Any Project

These instructions provide a tool-agnostic convention for automatically recording substantive AI use in any project. They may be used by individuals, teams, organizations, students, researchers, creators, developers, administrators, and others with Codex, Claude Code, or another AI system that can maintain project files.

## General Principles

- Be concrete and audit-friendly.
- Prefer exact file paths, commands, dates, model names, and verification results over vague summaries.
- Do not guess hidden runtime metadata. If a value is unavailable, write `Not exposed in this session`.
- When installing these instructions, never replace or discard an existing user instruction file. Preserve the user's instructions and merge this recording convention into the file, clearly separating the added material and avoiding duplicate copies.
- When multiple people use AI agents, keep histories separated by human collaborator or history-owner name.
- After substantive work, maintain a durable project-history record even when no other project file changed.
- Record the user's request, inputs examined, actions taken, files changed, outputs produced, verification performed, assumptions, and unresolved questions.
- Follow project rules for privacy, confidentiality, security, intellectual property, authorship, disclosure, version control, retention, and the approved location of AI-use records.
- Keep one authoritative active history for the whole project. Do not create competing histories merely because the work spans multiple repositories, applications, platforms, folders, or deliverables.
- Keep operating-system metadata, application session files, caches, temporary files, credentials, secrets, tokens, and confidential or restricted contents out of `project_history/`.
- Do not add project-specific `AGENTS.md` or `CLAUDE.md` files unless the user explicitly asks or the project truly needs its own rules. When a project uses a common parent workspace, prefer one root instruction file that governs all child repositories and project components.

## General Project History

For substantive AI-assisted work in any project, create or append to the project's established AI-use or project-history record. This includes work that creates, changes, inspects, diagnoses, plans, decides, verifies, summarizes, organizes, or advises.

First identify the project's established root: the highest practical folder that represents the user's intended project scope and contains or maps its relevant repositories, files, inputs, outputs, and deliverables. For a multi-repository project, use the common parent workspace. For a simpler single-repository or non-repository project, use its established root. Do not automatically use the current subdirectory when it is only one component of a larger project.

If the project has no established convention, use this default path at that root:

```text
project_history/Person_Name/YYYY-MM-DD by Agent.md
```

Replace `Agent` with the actual AI tool name. For example:

```text
project_history/Person_Name/YYYY-MM-DD by Codex.md
project_history/Person_Name/YYYY-MM-DD by Claude.md
```

Use one subfolder per human collaborator or history owner, with spaces converted to underscores, and identify the AI tool in the filename. For a solo project, use the user's name when known. If the history owner is unclear, ask when practical; otherwise use `Unknown_Collaborator` and record the uncertainty.

Use the history owner's local date and time zone. Create or append to the record at the end of each substantive task, including when the work only inspected materials, provided advice, made a decision, or performed verification. Do not overwrite earlier entries from the same day.

Do not include confidential, sensitive, proprietary, embargoed, regulated, security-relevant, or personally identifying information in the history unless the project permits it. The project history supplements rather than replaces any required audit log, change log, disclosure, compliance record, methods documentation, decision record, authorship statement, or other formal documentation.

## Project Root and Multi-Repository Projects

Use the simplest structure that represents the actual project. A general multi-repository project may look like:

```text
Project-Name/
├── AGENTS.md                   # optional project-specific rules
├── README.md                   # optional project map
├── project_history/
│   └── Person_Name/
│       └── YYYY-MM-DD by Agent.md
├── repository-one/
├── repository-two/
└── other-materials/
```

The common parent is the single AI workspace and does not need to be a Git repository. Keep exactly one active `project_history/` at this common root unless the user or organization intentionally defines another convention. Do not create separate active histories inside child repositories, mirrors, build folders, archives, exports, or deliverable folders.

Before changing a repository, shared document space, hosted service, or other stateful project component, inspect and respect its own version, synchronization, review, approval, access, and protection conventions. When outputs move between components, record the promotion, publication, export, or handoff step.

The root `README.md`, when used, should act as the project map. It may identify the project's purpose, owners, components, repositories and remotes, source-of-truth locations, sensitive-data boundaries, inputs, outputs, handoff or publication workflow, and current status.

## Examples of Projects

This convention can be used for:

- software development, websites, applications, and data systems;
- business, nonprofit, government, administrative, and operational projects;
- design, writing, publishing, media, and other creative work;
- teaching, coursework, training, and learning projects;
- research, manuscripts, data analysis, laboratories, and replication packages;
- event planning, personal organization, community work, and other structured projects.

Adapt the metadata to the project. Record repository state for code, document versions for writing, source files and exports for design, datasets and transformations for analysis, decisions and approvals for operations, and other evidence that makes the work understandable and auditable.

## Research and Replication Packages

Research projects may use a more specific common-root architecture with separate manuscript and analysis repositories. For replication-package work, follow the current [AI-Assisted Research Project Management and Replication Guide](https://yhoriuchi.github.io/replication-package-guide/) in addition to this general recording convention.

For replication-package work, the AI agent must:

- Read the current AI-Assisted Research Project Management and Replication Guide, the root `AGENTS.md` and `README.md`, and the target journal's most up-to-date official replication-package instructions before substantive work. The user may read these materials for context but is not responsible for studying the detailed operational requirements.
- Record each external source or supplied file and its access date.
- When journal instructions conflict with the replication guide, follow the journal for package requirements. For AI-use recording and history location, follow this AI Collaboration Guide and the root project instructions.
- Keep the project history private by default. Do not include it in the public replication package, manuscript repository, or journal submission unless the project explicitly requires disclosure there.
- Record the target journal, journal-specific requirements, restricted-data limits, manual steps, release artifacts, verification results, and unresolved reproducibility risks.

For multi-repository research projects, keep one history at the common research-project root rather than separate histories inside the manuscript repository, analysis repository, Overleaf mirror, public replication package, or submission folders. Keep raw or restricted data outside Git and outside an Overleaf-synchronized folder when required by law, policy, agreement, or ethics.

## Storage, Platforms, and Tools

Local folders, Git repositories, Overleaf, Dropbox, Google Drive, iCloud, SharePoint, Box, Notion, and other systems can all participate in a project. Keep the history at the established project root or another durable location explicitly chosen by the user or organization.

Cloud synchronization, version control, document history, and application storage have different scopes. Use approved storage and access controls. Do not copy confidential or restricted material into the history merely to make the log more detailed.

## Metadata Requirements

Record as much metadata as the AI agent can access.

Be maximally specific about model and runtime settings. Model recording is the AI agent's responsibility: obtain the information automatically from available task/runtime metadata and the AI interface whenever possible. Do not routinely ask the user to identify the model or reasoning setting, and do not require users to repeat those settings in each prompt. Treat settings explicitly stated by the user or visibly selected in the AI interface as exposed, authoritative session metadata; record them even when the underlying runtime configuration is not independently surfaced to the agent. Do not replace a known user-selected value with `Unknown`, `Not exposed in this session`, or a generic model family. Do not record a generic label such as `GPT-5` when a more specific model is known. Prefer exact display names and slugs such as:

- `GPT-5.5`
- `GPT-5.6 Terra`
- `GPT-5.6 Sol`
- `GPT-5.6 Luna`
- `Claude Opus`
- `Claude Sonnet`

Record both the human-readable reasoning effort and the raw/config value when known, for example:

```text
Light / low
Extra High / xhigh
High / high
```

If only the interface label is known, preserve that exact label and mark only the raw/config value as not exposed; do not mark the reasoning effort itself as unavailable. If a value truly is unavailable from the runtime, interface, and existing conversation context, say so rather than guessing. Ask the user about model metadata only when accurate attribution is materially necessary and cannot be obtained automatically; missing metadata alone should not interrupt ordinary work.

Record speed or service tier explicitly, for example:

```text
Fast
Priority
Flex
Not exposed in this session
```

Apply this metadata check to every appended task or follow-up entry, not only the first entry in a daily history file. Before finalizing each entry, cross-check the model display name, model family, model slug, reasoning-effort label, and raw/config value against all available session context and earlier same-session entries. Do not copy an earlier entry's metadata if the model or reasoning setting changed between tasks.

For every task entry, record separate fields for:

```text
Model display name:
Model family:
Model slug:
Reasoning level/effort:
Reasoning raw/config value:
Speed mode:
Service tier:
```

Use the exact values exposed for that task. For example:

```text
Model display name: GPT-5.6 Sol
Model family: GPT-5.6
Model slug: gpt-5.6-sol
Reasoning level/effort: Light
Reasoning raw/config value: low
Speed mode: Not exposed in this session
Service tier: Priority
```

The example illustrates the required level of detail; it is not a default model configuration. Codex, Claude, and other agents must record their own actual task-specific settings.

Metadata should include, when available:

- Date and time.
- Time zone.
- Human collaborator / history owner.
- AI agent/tool.
- Codex or Claude surface, such as desktop app, CLI, IDE, web, or cloud.
- Source task/thread identifier or description.
- Working directory.
- Project root and history location.
- Project name.
- Main artifact, deliverable, document, system, or workstream.
- Applicable organizational, legal, contractual, publication, platform, or domain-specific requirements checked.
- User-stated goal.
- Primary work type.
- Model display name.
- Model family.
- Model slug.
- Reasoning level/effort.
- Reasoning raw/config value.
- Verbosity.
- Speed mode.
- Service tier.
- Collaboration/planning mode.
- Sandbox/permissions.
- Approval policy.
- Network/web access.
- Active tools, skills, plugins, connectors, or MCP servers.
- Shell, OS, and relevant runtime/tool versions.
- Relevant repository remotes, branches, commits, ahead/behind states, and dirty-state summaries.
- Relevant document versions, dataset versions, application states, or external-system identifiers.
- Files inspected.
- Files changed.
- Files created, removed, relocated, staged, committed, pushed, or otherwise affected.
- Commands run.
- Verification commands and results.
- Outputs produced.
- Releases, deployments, exports, archives, manifests, checksums, logs, page counts, file sizes, record counts, or other concrete artifact metadata when relevant.
- Open questions or unresolved issues.

## Preferred History Structure

Use this structure unless the user or project asks for a different one:

```md
# YYYY-MM-DD by Agent

## Metadata

- Date:
- Time:
- Time zone:
- AI surface:
- Source task/thread:
- Model display name:
- Model family:
- Model slug:
- Reasoning level/effort:
- Reasoning raw/config value:
- Verbosity:
- Speed mode:
- Service tier:
- Collaboration/planning mode:
- Sandbox/permissions:
- Approval policy:
- Network/web access:
- Working directory:
- Human collaborator / history owner:
- History file path:
- Repository/repositories branch/commit/status:
- Main artifact/deliverable:
- Primary work type:
- User goal:
- Active tools/skills/plugins/connectors:
- Data, source files, and inputs used:
- Main commands:
- Verification status:

## Summary of User Instructions

- 

## Summary of Agent Work

- 

## Files Inspected

- 

## Files Changed

- 

## Files Created

- 

## Files Removed or Relocated

- 

## Outputs / Deliverables

- 

## Verification

- 

## External Sources Checked

- 

## Notes, Assumptions, and Open Questions

- 

## End-of-Day Status

- 
```
