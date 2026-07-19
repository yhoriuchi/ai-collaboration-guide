# Global Agent Instructions for Recording AI Use in Research

These instructions provide a tool-agnostic convention for automatically recording substantive AI use across research disciplines and project types. They may be adapted for Codex, Claude Code, or another AI system that can maintain project files.

## General Principles

- Be concrete and audit-friendly.
- Prefer exact file paths, commands, dates, model names, and verification results over vague summaries.
- Do not guess hidden runtime metadata. If a value is unavailable, write `Not exposed in this session`.
- When multiple collaborators use AI agents, keep histories separated by human collaborator name.
- After substantive work, maintain a durable project-history record even when no other project file changed.
- Record the user's request, inputs examined, actions taken, files changed, outputs produced, verification performed, assumptions, and unresolved questions.
- Follow project rules for privacy, confidential data, authorship, disclosure, version control, and the approved location of AI-use records.
- Do not add project-specific `AGENTS.md` or `CLAUDE.md` files unless the user explicitly asks or the project truly needs its own rules.

## General Research Project History

For substantive AI-assisted work in a research project, create or append to the project's established AI-use or project-history record. This applies to individual and collaborative work across disciplines, including manuscripts, data analysis, code, literature reviews, presentations, grant proposals, research administration, teaching materials, and other research-related artifacts.

If the project has no established convention, use the nearest project root and this default path:

```text
project_history/Person_Name/YYYY-MM-DD by Agent.md
```

Use one subfolder per human researcher, with spaces converted to underscores, and identify the AI tool in the filename. For a solo project, use the researcher's name. If the human history owner is unclear, ask when practical; otherwise use `Unknown_Researcher` and record the uncertainty.

Use the researcher's local date and time zone. Create or append to the record at the end of each substantive task, including when the work only inspected materials, provided advice, made a decision, or performed verification. Do not overwrite earlier entries from the same day.

Do not include confidential, sensitive, proprietary, embargoed, or personally identifying information in the history unless the project permits it. The project history supplements rather than replaces any required AI disclosure, methods documentation, data-management record, laboratory notebook, authorship statement, or ethics documentation.

## Worked Example: Dropbox + Overleaf + Codex

The author's worked example is a shared Overleaf project synchronized through Dropbox and opened as the working directory in Codex. Collaborators can continue writing in Overleaf while Codex works on the synchronized files and automatically maintains the project history described below.

This combination reflects the author's workflow; it is not a universal product recommendation. Claude Code and other file-capable AI assistants can follow the same recording standard. Preserve that standard when using another AI tool, storage service, document platform, or repository workflow, and adapt only the tool-specific setup and path conventions.

## GitHub-Centered Overleaf Workflow

As an alternative to the Dropbox-centered worked example, a project may use GitHub as its primary working repository and connect it to Overleaf through the project's GitHub integration.

- Do not require direct Overleaf access or assume that the working files live under the Overleaf Dropbox directory.
- A coding agent such as Codex or Claude can be given access to the GitHub repository and edit the manuscript sources through GitHub while coauthors use the connected Overleaf project.
- Before changing files, check the project's branch, commit, review, and synchronization conventions. Avoid overlapping unsynchronized edits in GitHub and Overleaf, and respect repository protections.
- The Overleaf project-history rule below applies when the working directory is inside the Overleaf Dropbox path. A GitHub-centered project elsewhere should follow its own repository and project-history conventions.

## Overleaf Project History

When working in any project under:

```text
~/Dropbox/Apps/Overleaf
```

maintain a daily AI project-history file.

For every substantive task whose working directory is inside an Overleaf project, create or append to:

```text
project_history/Person_Name/YYYY-MM-DD by Agent.md
```

Place the `project_history` directory at the Overleaf project root, not in a nested subdirectory.

Use one subfolder per human collaborator, with spaces converted to underscores.

Examples:

```text
project_history/Your_Name/YYYY-MM-DD by Codex.md
project_history/Your_Name/YYYY-MM-DD by Claude.md
project_history/Collaborator_Name/YYYY-MM-DD by Codex.md
project_history/Collaborator_Name/YYYY-MM-DD by Claude.md
```

Use the human collaborator's name for the subfolder, not the AI agent's name. If the collaborator is unclear, ask when practical. Otherwise use `Unknown_Collaborator` and record the uncertainty in metadata.

Use the local date in Eastern time. Use the AI agent/tool name in the filename, such as:

```text
YYYY-MM-DD by Codex.md
YYYY-MM-DD by Claude.md
```

Append to an existing daily file rather than overwriting it.

## R Package / Software Project History

When working in a shared software project or R package, maintain the same daily history convention at the nearest package/project root:

```text
project_history/Person_Name/YYYY-MM-DD by Agent.md
```

If the project has its own preferred history convention, follow that project-specific convention.

## Metadata Requirements

Record as much metadata as the AI agent can access.

Be maximally specific about model and runtime settings. Do not record a generic label such as `GPT-5` when a more specific model is exposed. Prefer exact display names and slugs such as:

- `GPT-5.5`
- `GPT-5.6 Terra`
- `GPT-5.6 Sol`
- `GPT-5.6 Luna`
- `Claude Opus`
- `Claude Sonnet`

Record both the human-readable reasoning effort and the raw/config value when possible, for example:

```text
Extra High / xhigh
High / high
```

Record speed or service tier explicitly, for example:

```text
Fast
Priority
Flex
Not exposed in this session
```

Metadata should include, when available:

- Date and time.
- Time zone.
- Human collaborator / history owner.
- AI agent/tool.
- Codex or Claude surface, such as desktop app, CLI, IDE, web, or cloud.
- Source task/thread identifier or description.
- Working directory.
- Project name.
- Manuscript, paper, package, or artifact title.
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
- Sandbox/permissions.
- Approval policy.
- Network/web access.
- Active tools, skills, plugins, connectors, or MCP servers.
- Shell, OS, and relevant runtime/tool versions.
- Git branch, commit, and dirty-state summary when relevant.
- Files inspected.
- Files changed.
- Commands run.
- Verification commands and results.
- Outputs produced.
- Open questions or unresolved issues.

## Preferred History Structure

Use this structure unless the user or project asks for a different one:

```md
# YYYY-MM-DD by Agent

## Metadata

- Date:
- Time:
- Time zone:
- Human collaborator / history owner:
- History file path:
- AI agent/tool:
- Agent surface:
- Source task/thread:
- Model display name:
- Model family:
- Model slug:
- Reasoning level/effort:
- Reasoning raw/config value:
- Verbosity:
- Speed mode:
- Service tier:
- Sandbox/permissions:
- Approval policy:
- Network/web access:
- Working directory:
- Project:
- Manuscript/package/artifact:
- Primary work type:
- User goal:
- Active tools/skills/plugins/connectors:
- Data, source files, and inputs used:
- Main commands:
- Verification status:

## Summary of User Instructions

- 

## Summary of AI Work

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
