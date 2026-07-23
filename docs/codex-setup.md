# Codex Setup

This setup implements the tool-agnostic recording convention with Codex for any kind of project. Copy the setup prompt below, paste it into Codex, and approve the file write if Codex asks. Codex should install the shared global instructions automatically without replacing any instructions you already have.

## Setup Prompt

```text
Please install the shared instructions for automatically recording substantive AI use across my projects with Codex.

1. Fetch the current AGENTS.md from:
   https://raw.githubusercontent.com/yhoriuchi/ai-collaboration-guide/main/AGENTS.md
2. Create ~/.codex if it does not exist.
3. Inspect ~/.codex/AGENTS.md if it already exists. Never overwrite or discard existing user instructions.
4. If ~/.codex/AGENTS.md does not exist, save the fetched content there. If it does exist, merge the fetched instructions into it while preserving all existing content. Put the new material in a clearly labeled section, avoid adding a duplicate if this recording convention is already present, and report any direct conflict instead of silently resolving it.
5. Do not modify any project files during this setup.
6. Confirm the final file path, whether the file was created or merged, and whether any network or file-write permission was needed.
```

## Create or Open a Codex Project

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

After that, prompt Codex in whatever way is natural for the task.

Replace `Your_Name` with your collaborator folder name, for example:

```text
Your_Name
Collaborator_Name
```

You do not need to manually create the history log each time. The shared instructions ask Codex to create or append it automatically.

For replication-package work, also direct Codex to read the current [Replication Package Guide](https://yhoriuchi.github.io/replication-package-guide/), the root `AGENTS.md` and `README.md`, and the target journal's current official replication-package instructions before substantive work.

If Codex cannot access the URL automatically, open `AGENTS.md` from this repository and ask Codex to install that content in `~/.codex/AGENTS.md` using the same preserve-and-merge procedure above.
