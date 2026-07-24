# Claude Code Setup

This setup implements the same tool-agnostic recording convention with Claude Code for any kind of project. Copy the setup prompt below, paste it into Claude Code, and approve the file write if Claude asks. Claude should install the shared global instructions automatically without replacing any instructions you already have.

## Setup Prompt

```text
Please install the shared instructions for automatically recording substantive AI use across my projects with Claude Code.

1. Fetch the current AGENTS.md from:
   https://raw.githubusercontent.com/yhoriuchi/ai-collaboration-guide/main/AGENTS.md
2. Create ~/.claude if it does not exist.
3. Inspect ~/.claude/AGENTS.md if it already exists. Never overwrite or discard existing user instructions.
4. If ~/.claude/AGENTS.md does not exist, save the fetched content there. If it does exist, merge the fetched instructions into it while preserving all existing content. Put the new material in a clearly labeled section, avoid adding a duplicate if this recording convention is already present, and report any direct conflict instead of silently resolving it.
5. Inspect ~/.claude/CLAUDE.md if it already exists. Preserve all existing content and ensure that it contains this import line, adding the line only if it is absent:
   @~/.claude/AGENTS.md
6. Do not modify any project files during this setup.
7. Confirm the final file paths, whether each file was created or merged, and whether any network or file-write permission was needed.
```

## Create or Open a Claude Code Project

Choose the working directory that represents the whole project:

- **Simple project:** choose the established project folder or repository.

- **Multi-repository or multi-component project:** choose the common parent:

```text
Project-Name/
├── AGENTS.md                   # optional project rules
├── README.md                   # optional project map
├── project_history/
├── repository-one/
├── repository-two/
└── other-materials/
```

Keep exactly one active `project_history/` at the project root unless the user or organization deliberately chooses another convention. Do not create separate histories inside child repositories, mirrors, build folders, archives, exports, or deliverable folders.

Use storage, version control, document platforms, access controls, and retention policies appropriate to the project. Do not copy confidential, restricted, regulated, or security-relevant material into the history unless permitted.

After that, prompt Claude in whatever way is natural for the task.

You do not need to manually create the history log each time. The shared instructions ask Claude to create or append it automatically.

For replication-package work, also direct Claude to read the current [AI-Assisted Research Project Management and Replication Guide](https://yhoriuchi.github.io/replication-package-guide/), the root `AGENTS.md` and `README.md`, and the target journal's current official replication-package instructions before substantive work.

If Claude cannot access the URL automatically, open `AGENTS.md` from this repository and ask Claude to install that content in `~/.claude/AGENTS.md` using the same preserve-and-merge procedure above, then ensure that `~/.claude/CLAUDE.md` contains `@~/.claude/AGENTS.md` without replacing its existing content.

## Reference

Claude Code memory docs:

https://code.claude.com/docs/en/memory
