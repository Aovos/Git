# Committing Changes

> A commit creates a snapshot of all currently staged changes.
> > Each commit represents a specific state of your repository and is stored in the repository history.
> > Commits allow you to track, review, and restore previous versions of your work.

1. Create a commit with a descriptive message:

```bash
git commit -m "Your commit message"
```

Example:

```bash
git commit -m "Add repository status section"
```

## Commit Messages

> A commit message should briefly describe the purpose of the changes.

Good examples:

- Add repository status section
- Fix typo in Git documentation
- Update installation instructions

Bad examples:

- Update
- Changes
- Fix

> Write meaningful commit messages so you can easily understand the purpose of each commit when reviewing the repository history.

## Verify the Commit

1. Display the commit history:

```bash
git log
```

2. Display a compact version of the commit history:

```bash
git log --oneline
```

> Your newly created commit should appear in the output.

Example output:

> a1b2c3d Add repository status section
