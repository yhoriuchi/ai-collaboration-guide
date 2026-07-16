# Codex Setup

This is meant to be easy. Collaborators can keep writing and revising in Overleaf as usual. The only Codex setup is to install the shared instructions and choose the existing Overleaf project folder as the Codex working directory.

## Install Global Instructions

Copy the shared `AGENTS.md` file to:

```text
~/.codex/AGENTS.md
```

Codex reads this global file automatically.

## Create or Open a Codex Project

In Codex, create/open a project and choose the existing Overleaf project folder as the working directory:

```text
~/Dropbox/Apps/Overleaf/Project-Name
```

Do not reorganize Dropbox folders. The folder only matters because Codex needs a project directory.

After that, prompt Codex in whatever way is natural for the task. A useful first message is:

```text
We are working in a shared Overleaf or research project.
Follow the global AGENTS/CLAUDE instructions.
Treat the current folder as the project root unless told otherwise.
Save today's project history under project_history/Your_Name/YYYY-MM-DD by Agent.md.
Record the exact model, reasoning effort, speed/service tier, files changed, commands run, and verification.
```

Replace `Your_Name` with your collaborator folder name, for example:

```text
Your_Name
Collaborator_Name
```

You do not need to manually create the history log each time. The shared instructions ask Codex to create or append it automatically.
