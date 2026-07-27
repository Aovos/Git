# Git


[Installation](#installation)

[Git Identity](#git-identity)

[Creating a Repository](#creating-a-repository)

[Repository Status](#repository-status)


## Installation
> Check if `Git` is already installed on your system.
```bash
git --version
```
> If a version number is displayed, you are ready to proceed
> > otherwise, you must install Git first.


### Debian

```bash
sudo apt update
sudo apt install git
```

### NixOS

> Go to your NixOS configuration: `/etc/nixos/configuration.nix`:
> > Paste `git` inside the `systemPackages`
```nix
environment.systemPackages = with pkgs; [
  git
];
```

> After that, rebuild your NixOS system and switch to it:
```bash
sudo nixos-rebuild switch
```


## Git Identity

### Global Identity Configuration

> Applies to all repositories by default.
> > Set your global `username` and `e-mail`:
```bash
git config --global user.name "Your Name"
git config --global user.email "Your e-mail"
```
> Check the global identity configuration
```bash
git config --global user.name
git config --global user.email
```

### Local Identity Configuration

> Applies only to the current repository and overrides the global configuration.
> > Navigate to your repository:


```bash
cd your-repository
```

> Set your local `username` and `e-mail`:

```bash
git config user.name "Your Name"
git config user.email "Your e-mail"
```

> Check the local identity configuration

```bash
git config user.name
git config user.email
```


## Creating a Repository

### Standard Repository
> A standard repository contains both your `working directory` and the `Git metadata` in the same folder.
> > Navigate to the directory where you want to create your repository:
```bash
cd your-path
```

> Initialize a standard Git repository:
```bash
git init
```

> Git will create a hidden `.git` directory inside your current working directory.
> > This directory contains all repository metadata.
> > Verify that the repository was created:

```bash
ls -la
```
> You should see a `.git` directory in the output.


### Bare Repository

> Unlike a standard repository, a bare repository contains only Git metadata.
> > Bare repositories are commonly used as central remote repositories or when Git metadata should be stored separately from the working directory.

> Navigate to the directory where you want to create your bare repository:
> > For example, you can create a parent directory such as `~/Git` in your home directory and store individual repositories in separate subdirectories like `~/Git/dotfiles`.

```bash
cd your-path
```

> Create a directory for the repository:

```bash
mkdir my-repository.git
```

> Navigate into the repository directory:

```bash
cd my-repository.git
```

> Initialize a bare Git repository:

```bash
git init --bare
```

> Verify that the repository was created:

```bash
ls -la
```
> Unlike a standard repository, no `.git` directory exists.
> > The repository itself contains all Git metadata.


## Repository Status

> Displays the current state of your repository.
> > Shows tracked files, untracked files, staged changes, and pending commits.
```bash
git status
```
> Example output:
```text
On branch main
No commits yet
nothing to commit (create/copy files and use "git add" to track)
```
> Run this command regularly to see what has changed in your repository.


## Staging Files

> Before changes can be committed, they must be added to the staging area.
> > The staging area acts like a queue for the next commit, allowing you to choose exactly which changes should be included.
> > > There are two main methods to stage changes: staging specific files or staging all changes at once.

### Stage Specific Files

> Stage one specific file:
```bash
git add my-file.txt
```

> Multiple files can be staged at the same time:
```bash
git add file-1.txt file-2.txt file-3.txt
```

### Stage All Changes

> Stage all modified and untracked files in the current directory and its subdirectories:
```bash
git add .
```

> Always check the current repository status:
```bash
git status
```
> Files listed under `Changes to be committed` are staged and ready to be committed.
> Files listed under `Changes not staged for commit` are modified but not yet staged.
