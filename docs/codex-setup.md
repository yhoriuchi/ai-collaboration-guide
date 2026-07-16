# Codex Setup

Collaborators can keep writing and revising in Overleaf. The Dropbox-synced Overleaf folder is used as the Codex project working directory so Codex can inspect/edit files and save history logs.

## Install Global Instructions

Copy the shared `AGENTS.md` file to:

```text
~/.codex/AGENTS.md
```

Codex reads this global file automatically.

## Create or Open a Codex Project

In Codex, create/open a project and set the working directory to the Dropbox-synced Overleaf project folder:

```text
~/Dropbox/Apps/Overleaf/Project-Name
```

After that, prompt Codex in whatever way is natural for the task. A useful first message is:

```text
This Codex project uses the Dropbox-synced Overleaf folder as its working directory.
Please follow the shared AGENTS instructions and save the project_history log automatically.
```

Replace `Your_Name` with your collaborator folder name, for example:

```text
Yusaku_Horiuchi
Huijie_Xu
```

You do not need to manually create the history log each time. The shared instructions ask Codex to create or append it.
