# Git

> A beginner-friendly guide covering Git fundamentals, repository management, version control, and collaboration workflows.


## Basics

| Guide | Command | Description |
|---------|---------|---------|
| [Git Installation](Git-Installation.md) | `git --version` | Check if Git is installed |
| | `sudo apt install git` | Install Git on Debian-based systems |
| | `sudo nixos-rebuild switch` | Apply the NixOS configuration |
| [Git Identity](Git-Identity.md) | `git config --global user.name "Your Name"` | Configure the global username |
| | `git config --global user.email "you@example.com"` | Configure the global e-mail address |
| | `git config user.name "Your Name"` | Configure a local username |
| | `git config user.email "you@example.com"` | Configure a local e-mail address |
| [Creating a Repository](Creating-a-Repository.md) | `git init` | Create a standard repository |
| | `git init --bare` | Create a bare repository |
| [Cloning Repositories](Cloning.md) | `git clone URL` | Clone an existing repository |
| [Ignoring Files](Gitignore.md) | `touch .gitignore` | Create a `.gitignore` file |
| | `git rm --cached file.txt` | Stop tracking a file while keeping it on disk |
| [Repository Status](Repository-Status.md) | `git status` | Display the current repository state |
| [Staging Files](Staging-Files.md) | `git add my-file.txt` | Stage a specific file |
| | `git add file-1.txt file-2.txt` | Stage multiple files |
| | `git add .` | Stage all changes in the current directory |
| [Committing Changes](Committing-Changes.md) | `git commit -m "message"` | Create a new commit |
| [Viewing Commit History](Viewing-Commit-History.md) | `git log` | Display the full commit history |
| | `git log --oneline` | Display a compact commit history |
| | `git log -5` | Display the latest 5 commits |
| | `git show COMMIT_HASH` | Display detailed information about a commit |


## Inspecting Changes

| Guide | Command | Description |
|---------|---------|---------|
| Viewing-Differences.md | `git diff` | Show unstaged changes |
| | `git diff --staged` | Show staged changes |
| | `git diff branch-a..branch-b` | Compare two branches |
| [Viewing Commit History](Viewing-Commit-History.md) | `git log --graph --oneline --all` | Visualize repository history |
| | `git blame file.txt` | Show who modified each line |



## Working with Changes

| Guide | Command | Description |
|---------|---------|---------|
| [Undoing Changes](Undoing-Changes.md) | `git restore my-file.txt` | Discard unstaged changes |
| | `git restore --staged my-file.txt` | Unstage a specific file |
| | `git restore --staged .` | Unstage all staged files |
| | `git revert COMMIT_HASH` | Create a commit that reverts previous changes |
| | `git checkout COMMIT_HASH` | View a previous commit |
| | `git reset --hard COMMIT_HASH` | Reset a branch to a specific commit ⚠️ |

### Warning

⚠️ `git reset --hard` permanently discards uncommitted changes and can rewrite branch history. Use it with caution.


## Collaboration

| Guide | Command | Description |
|---------|---------|---------|
| [Branches](Branches.md) | `git branch` | List local branches |
| | `git branch branch-name` | Create a new branch |
| | `git branch -d branch-name` | Delete a merged branch |
| | `git switch branch-name` | Switch to an existing branch |
| | `git switch -c branch-name` | Create and switch to a new branch |
| | `git checkout branch-name` | Switch branches (legacy method) |
| [Merging](Merging.md) | `git merge branch-name` | Merge a branch into the current branch |
| | `git status` | View files with merge conflicts |
| | `git add resolved-file.txt` | Mark a conflict as resolved |
| | `git merge --continue` | Continue the merge after resolving conflicts |
| [Remotes](Remotes.md) | `git remote -v` | List configured remotes |
| | `git remote add origin URL` | Add a remote repository |
| | `git remote remove origin` | Remove a remote repository |
| [Cloning Repositories](Cloning.md) | `git clone URL` | Clone an existing repository |
| [Pulling Changes](Pull.md) | `git pull` | Fetch and merge remote changes |
| | `git pull origin main` | Pull changes from a specific branch |
| [Pushing Changes](Push.md) | `git push` | Push changes to the remote repository |
| | `git push origin main` | Push changes to a specific branch |
| | `git push -u origin main` | Push and set the upstream branch |
| Pull-Requests.md | Platform-specific feature | Request code review before merging changes |


## Common Workflow

### Clone an Existing Repository

```bash
git clone URL
cd repository
```

### Create a New Repository

```bash
git init
touch .gitignore
git add .
git commit -m "Initial commit"
```

### Daily Workflow

```bash
git pull
git status
git add .
git commit -m "Describe your changes"
git push
```

### Feature Branch Workflow

```bash
git switch -c feature/my-feature

# Make changes

git add .
git commit -m "Add new feature"

git switch main
git pull

git merge feature/my-feature
git push
```


## Quick Reference

### Repository Management

```bash
git init
git clone URL
git status
```

### Staging & Committing

```bash
git add .
git commit -m "message"
```

### History & Inspection

```bash
git log --oneline
git show COMMIT_HASH
git diff
git blame file.txt
```

### Branches

```bash
git branch
git switch branch-name
git switch -c branch-name
git merge branch-name
```

### Remotes

```bash
git remote -v
git pull
git push
```

### Undo Operations

```bash
git restore file.txt
git restore --staged file.txt
git revert COMMIT_HASH
```


## Learning Path

If you're new to Git, follow the guides in this order:

1. Git Installation
2. Git Identity
3. Creating a Repository
4. Repository Status
5. Staging Files
6. Committing Changes
7. Viewing Commit History
8. Ignoring Files
9. Undoing Changes
10. Branches
11. Merging
12. Remotes
13. Pulling Changes
14. Pushing Changes
15. Pull Requests

By the end of these guides, you'll be able to manage repositories, track changes, collaborate with others, and confidently use Git in day-to-day development workflows.
