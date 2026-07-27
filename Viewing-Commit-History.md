# Viewing Commit History

> Git stores every commit in the repository history.
> > The commit history allows you to review previous changes and track the evolution of your repository.

## Display the Full Commit History

1. Show all commits with detailed information:

```bash
git log
```

The output includes:
- Commit hash
- Author
- Date
- Commit message

## Display a Compact Commit History

1. Show each commit in a single line:

```bash
git log --oneline
```

Example output:

```bash
a1b2c3d Add committing changes section
e4f5g6h Add staging files section
i7j8k9l Add repository status section
```

## Limit the Number of Results

1. Show only the most recent commits:

```bash
git log -5
```

> Displays only the last 5 commits.

## Display Changes of a Commit

1. Show detailed information about a specific commit:

```bash
git show COMMIT_HASH
```

Example:

```bash
git show a1b2c3d
```

Displays:
- Commit metadata
- Changed files
- Added lines
- Removed lines

## Useful Commit History Commands

1. Display a compact commit history with branch references:

```bash
git log --oneline --decorate
```

2. Display a graphical representation of the commit history:

```bash
git log --oneline --graph
```

> Useful when working with branches and merges.
