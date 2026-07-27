# Undoing Changes

> Git provides multiple ways to undo changes.
> > Depending on the situation, you can undo local changes, remove files from the staging area, or return to a previous version of your repository.

## Undo Local Changes

> Undo changes that have not yet been committed.

### Discard Unstaged Changes

1. Restore a file to its last committed state:

```bash
git restore my-file.txt
```

> Any unstaged changes in the file will be permanently lost.

### Unstage a File

1. Remove a file from the staging area while keeping the file changes:

```bash
git restore --staged my-file.txt
```

> The file remains modified but will no longer be included in the next commit.

### Unstage All Files

1. Remove all staged files from the staging area:

```bash
git restore --staged .
```

> All changes remain in your working directory.

## Undo Committed Changes

> Undo changes that are already part of the repository history.

### Revert a Commit

1. Create a new commit that reverses the changes of a previous commit:

```bash
git revert COMMIT_HASH
```

> The original commit remains in the repository history.
> > This is the safest method when working with shared repositories.

### Reset a Branch

1. Move the current branch back to a specific commit:

```bash
git reset --hard COMMIT_HASH
```

> Commits created after the target commit will no longer be part of the current branch history.
> > Use this command carefully, as changes may be difficult to recover.

### View a Previous Commit

1. Temporarily switch to a previous commit:

```bash
git checkout COMMIT_HASH
```

> This allows you to inspect an older version of the repository.
> > The commit history remains unchanged.
