# Commit Changes

> A commit creates a snapshot of all currently staged changes.
>
> Each commit represents a specific state of your repository and is stored in the repository history.
>
> Commits allow you to track, review, and restore previous versions of your work.
>
> Git only includes staged changes in a commit. Changes that have not been staged remain in the working directory and are not included.

1. Create a commit:

> Replace `"Your commit message"` with a short description of the changes included in the commit.

```bash
git commit -m "Your commit message"
```

Example:

```bash
git commit -m "Add repository status section"
```

Example output:

```text
[main abc1234] Add repository status section
 2 files changed, 15 insertions(+)
```

## Commit Messages

> Commit messages should clearly describe the purpose of the changes, making it easier to understand the repository history.

Good examples:

- Add repository status section
- Fix typo in Git documentation
- Update installation instructions

Bad examples:

- Update
- Changes
- Fix
