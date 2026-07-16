# Global Agent Instructions for Collaborative Research Projects

These instructions are intended for AI agents such as Codex and Claude Code.

Copy this file to:

```text
~/.codex/AGENTS.md
```

For Claude Code, copy this file to:

```text
~/.claude/AGENTS.md
```

and use `CLAUDE.md` to import it.

## General Principles

- Be concrete and audit-friendly.
- Prefer exact file paths, commands, dates, model names, and verification results over vague summaries.
- Do not guess hidden runtime metadata. If a value is unavailable, write `Not exposed in this session`.
- When multiple collaborators use AI agents, keep histories separated by human collaborator name.
- Do not add project-specific `AGENTS.md` or `CLAUDE.md` files unless the user explicitly asks or the project truly needs its own rules.

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

## First Prompt Template

At the beginning of a task, use or adapt:

```text
We are working in a shared Overleaf or research project.
Follow the global AGENTS/CLAUDE instructions.
Treat the current folder as the project root unless told otherwise.
Save today's project history under project_history/Your_Name/YYYY-MM-DD by Agent.md.
Record exact model, reasoning effort, speed/service tier, files changed, commands run, and verification.
```
