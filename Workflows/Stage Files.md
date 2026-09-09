# Stage Files

> Before changes can be committed, they must be added to the staging area.
>
> The staging area acts as a queue for the next commit, allowing you to choose exactly which changes should be included.
>
> There are two main methods to stage changes:
>
> - staging specific files
> - staging all changes at once

## Stage Specific Files

> Only the specified files will be added to the staging area.

- Stage a specific file:

```bash
git add my-file.txt
```

- Stage multiple files at the same time:

```bash
git add file-1.txt file-2.txt file-3.txt
```

## Stage All Changes

> This includes:
>
> - Modified tracked files
> - Untracked files
> - Newly created untracked files

```bash
git add .
```

## Unstage Files

> This removes files from the staging area but keeps all changes in your working directory.

- Unstage a specific file:

```bash
git restore --staged my-file.txt
```

- Unstage all staged files:

```bash
git restore --staged .
```
