# Project History Convention

Every substantive AI-assisted task should create or append to a Markdown history file.

## Folder and File Name

Use:

```text
project_history/Person_Name/YYYY-MM-DD by Agent.md
```

Examples:

```text
project_history/Yusaku_Horiuchi/2026-07-15 by Codex.md
project_history/Yusaku_Horiuchi/2026-07-15 by Claude.md
project_history/Huijie_Xu/2026-07-15 by Codex.md
project_history/Huijie_Xu/2026-07-15 by Claude.md
```

## Rules

- Put `project_history` at the project root.
- Use one subfolder per human collaborator.
- Use the AI agent name in the file name.
- Append to an existing daily file.
- Do not overwrite earlier entries.
- If no files changed, still record what was inspected, decided, or verified.

## Metadata

Record exact model and runtime details when exposed:

- Model display name.
- Model slug.
- Reasoning level/effort.
- Raw reasoning value.
- Speed mode.
- Service tier.
- Tool surface.
- Commands run.
- Verification.

If unavailable, write:

```text
Not exposed in this session
```
