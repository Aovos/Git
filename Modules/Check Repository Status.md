# Check Repository Status

> The repository status shows the current state of your working directory and staging area.
>
> Common Repository Statuses are `untracked`, `modified`, and `staged files`.

1. Navigate to your repository:

    ```bash
    cd /path/to/repository
    ```

2. Display the repository status:

    ```bash
    git status
    ```

## Common Repository Statuses

### Untracked Files

> Untracked files are files that Git is not currently tracking.

Example output:

```text
Untracked files:
  README.md
```

### Modified Files

> Modified files contain changes that have not been staged.

Example output:

```text
Changes not staged for commit:
  modified: README.md
```

### Staged Files

> Staged files are ready to be included in the next commit.

Example output:

```text
Changes to be committed:
  new file: README.md
```

### Clean Working Tree

> A clean working tree means there are no changes to commit.

Example output:

```text
On branch main
nothing to commit, working tree clean
```
