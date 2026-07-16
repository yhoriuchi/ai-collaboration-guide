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
This Codex project uses the existing Overleaf project folder as its working directory.
Please follow the shared AGENTS instructions and save the project_history log automatically.
```

Replace `Your_Name` with your collaborator folder name, for example:

```text
Yusaku_Horiuchi
Huijie_Xu
```

You do not need to manually create the history log each time. The shared instructions ask Codex to create or append it automatically.
