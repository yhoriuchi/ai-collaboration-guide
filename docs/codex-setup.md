# Codex Setup

This is meant to be easy. Copy the setup prompt below, paste it into Codex, and approve the file write if Codex asks. Codex should save the shared global instructions automatically.

## Setup Prompt

```text
Please install the shared Overleaf-project agent instructions for Codex.

1. Fetch the current AGENTS.md from:
   https://raw.githubusercontent.com/yhoriuchi/ai-collaboration-guide/main/AGENTS.md
2. Create ~/.codex if it does not exist.
3. Save the fetched content exactly to:
   ~/.codex/AGENTS.md
4. Do not modify any Overleaf project files during this setup.
5. Confirm the final file path and mention whether any network or file-write permission was needed.
```

## Create or Open a Codex Project

Choose the working directory that matches the project's collaboration path:

- **Direct Overleaf:** choose the existing Overleaf project folder:

```text
~/Dropbox/Apps/Overleaf/Project-Name
```

- **GitHub-centered alternative:** choose a local clone of the repository connected to Overleaf. Authors can use their preferred editor, and Codex can work through its GitHub access rather than direct Overleaf access.

Do not reorganize Dropbox folders or repository files merely for setup. Before editing in the GitHub-centered workflow, follow the project's branch, commit, review, and synchronization conventions; do not make overlapping unsynchronized edits in GitHub and Overleaf.

After that, prompt Codex in whatever way is natural for the task.

Replace `Your_Name` with your collaborator folder name, for example:

```text
Your_Name
Collaborator_Name
```

You do not need to manually create the history log each time. The shared instructions ask Codex to create or append it automatically.

If Codex cannot access the URL automatically, open `AGENTS.md` from this repository and ask Codex to save that content to `~/.codex/AGENTS.md`.

