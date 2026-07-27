# Git

> A beginner-friendly guide covering Git fundamentals, repository management, version control, and collaboration workflows.

## Basics

| Guide | Command | Description |
|---------|---------|---------|
| [Git Installation](Git-Installation.md) | `git --version` | Check if Git is installed |
| | `sudo apt install git` | Install Git on Debian |
| | `sudo nixos-rebuild switch` | Apply the NixOS configuration |
| [Git Identity](Git-Identity.md) | `git config --global user.name "Your Name"` | Configure the global username |
| | `git config --global user.email "you@example.com"` | Configure the global e-mail address |
| | `git config user.name "Your Name"` | Configure a local username |
| | `git config user.email "you@example.com"` | Configure a local e-mail address |
| [Creating a Repository](Creating-a-Repository.md) | `git init` | Create a standard repository |
| | `git init --bare` | Create a bare repository |
| [Repository Status](Repository-Status.md) | `git status` | Display the current repository state |
| [Staging Files](Staging-Files.md) | `git add my-file.txt` | Stage a specific file |
| | `git add file-1.txt file-2.txt` | Stage multiple files |
| | `git add .` | Stage all changes in the current directory |
| [Committing Changes](Committing-Changes.md) | `git commit -m "message"` | Create a new commit |
| [Viewing Commit History](Viewing-Commit-History.md) | `git log` | Display the full commit history |
| | `git log --oneline` | Display a compact commit history |
| | `git log -5` | Display the latest 5 commits |
| | `git show COMMIT_HASH` | Display detailed information about a commit |


## Working with Changes

| Guide | Command | Description |
|---------|---------|---------|
| [Ignoring Files](Gitignore.md) | `touch .gitignore` | Create a `.gitignore` file |
| | `git rm --cached secret.txt` | Stop tracking a file while keeping it on disk |
| [Undoing Changes](Undoing-Changes.md) | `git restore my-file.txt` | Discard unstaged changes |
| | `git restore --staged my-file.txt` | Unstage a specific file |
| | `git restore --staged .` | Unstage all staged files |
| | `git revert COMMIT_HASH` | Revert a previous commit |
| | `git reset --hard COMMIT_HASH` | Reset a branch to a specific commit |
| | `git checkout COMMIT_HASH` | View a previous commit |


## Collaboration

- [Branches](Branches.md)
- [Merging](Merging.md)
- [Remotes](Remotes.md)
- [Cloning Repositories](Cloning.md)
- [Pushing Changes](Push.md)
- [Pulling Changes](Pull.md)
