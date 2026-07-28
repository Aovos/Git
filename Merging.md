# Git Merging

> Merging combines the history and changes from two different branches. Most commonly, you use this to integrate a finished feature branch back into the main branch (`main` or `master`).

## Merging Changes

> Integrates the commits from another branch into your current branch.

1. First, switch to the branch that should *receive* the changes (e.g., `main`):

```bash
git checkout main
```
*(Alternative):*
```bash
git switch main
```

2. Merge the feature branch into your current branch:

```bash
git merge feature-new-function
```

> If there are no conflicts, Git will automatically create a new "Merge Commit" or perform a "Fast-Forward" merge.

## Resolving Merge Conflicts

> Occurs when the same line in the same file has been modified differently in both branches. Git will pause the merge process and ask you to clean it up manually.

1. View the status of the conflicted files:

```bash
git status
```

2. Open the flagged files. Git highlights conflicts using special markers:

```text
<<<<<<< HEAD
Your code in the current branch (e.g., main)
=======
The code from the branch you want to merge in (e.g., feature-new-function)
>>>>>>> feature-new-function
```

3. Clean up the file manually (remove the `<<<<<<<`, `=======`, `>>>>>>>` markers and choose which code to keep).

4. Add the resolved files to the staging area and finalize the merge:

```bash
git add file-with-conflict.txt
git commit -m "chore: resolve merge conflict"
```

## Aborting a Merge

> Completely resets your workspace to its state before the merge started, which is useful if something goes wrong while resolving conflicts.

1. Abort the ongoing merge process:

```bash
git merge --abort
```
