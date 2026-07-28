# Git Branches

> Branches allow you to work on new features or bug fixes independently from the main codebase (usually `main` or `master`), without risking the stability of production code.

## Managing and Listing Branches

> Lists all existing branches and indicates which branch you are currently working on.

1. List local branches:

```bash
git branch
```

2. List all local and remote branches:

```bash
git branch -a
```

> The current branch will be marked with an asterisk (`*`) in the output.

## Creating a New Branch

> Creates an exact copy of your current working state under a new name.

1. Create a new branch:

```bash
git branch feature-new-function
```

> This command only creates the branch. It does not automatically switch your workspace to it.

## Switching Branches

> Switches your workspace to another existing branch.

1. Switch to an existing branch:

```bash
git checkout feature-new-function
```
*(Alternative):*
```bash
git switch feature-new-function
```

2. Create a new branch and switch to it immediately:

```bash
git checkout -b feature-new-function
```
*(Alternative):*
```bash
git switch -c feature-new-function
```

## Deleting Branches

> Removes branches that are no longer needed (e.g., after a successful merge).

1. Safely delete a branch (fails if changes are not fully merged):

```bash
git branch -d feature-new-function
```

2. Force delete a branch (will delete unmerged changes as well):

```bash
git branch -D feature-new-function
```
