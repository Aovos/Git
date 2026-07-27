# Staging Files

> Before changes can be committed, they must be added to the staging area.
> > The staging area acts like a queue for the next commit, allowing you to choose exactly which changes should be included.
> > There are two main methods to stage changes:
> > - staging specific files
> > - staging all changes at once.

## Stage Specific Files

- Stage a specific file:

```bash
git add my-file.txt
```

- Stage multiple files at the same time:

```bash
git add file-1.txt file-2.txt file-3.txt
```

> Only the specified files will be added to the staging area.

## Stage All Changes

- Stage all modified and untracked files in the current directory and its subdirectories:

```bash
git add .
```

> This includes:
> - Modified tracked files
> - Newly created untracked files

## Stage Status
> Always verify your staged files before creating a commit to ensure only the intended changes are included.
- Check the repository status:

```bash
git status
```

> Files listed under `Changes to be committed` are staged and ready for the next commit.

Example output:

```text
Changes to be committed:
  modified: README.md
  new file: Staging.md
```

> Files listed under `Changes not staged for commit` contain modifications that have not yet been staged.

Example output:

```text
Changes not staged for commit:
  modified: README.md
```
