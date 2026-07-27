# Repository Status

> Repository status provides an overview of the current state of your repository.
> > It helps you identify modified, untracked, staged, and committed files before performing Git operations.

1. Display the current repository status:

```bash
git status
```

> Git will display information about:
> - Tracked files
> - Untracked files
> - Staged changes
> - Unstaged changes
> - The currently active branch

Example output:

```text
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

2. Review the output:

> Files listed under `Changes to be committed` are staged and ready for the next commit.

> Files listed under `Changes not staged for commit` contain modifications that have not yet been staged.

> Files listed under `Untracked files` are not currently tracked by Git.

3. Run this command regularly:

```bash
git status
```

> This is one of the most frequently used Git commands.
> > It should be used before staging, committing, pulling, merging, or pushing changes.
