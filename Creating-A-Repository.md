# Creating a Repository

> A Git repository is the storage location for your project's files, history, branches, and metadata.
> > Git provides two repository types: standard repositories and bare repositories.

## Standard Repository

> A standard repository contains both your working directory and the Git metadata in the same location.

1. Navigate to the directory where you want to create your repository:

```bash
cd your-path
```

2. Initialize a standard Git repository:

```bash
git init
```

> Git will create a hidden `.git` directory inside your current working directory. This directory contains all repository metadata.

3. Verify that the repository was created:

```bash
ls -la
```

> You should see a `.git` directory in the output.

Example output:

```text
.
..
.git
```

## Bare Repository

> Unlike a standard repository, a bare repository contains only Git metadata.
> > Bare repositories are commonly used as central remote repositories or when Git metadata should be stored separately from the working directory.

1. Navigate to the directory where you want to create your bare repository:

```bash
cd your-path
```

2. Create a directory for the repository:

```bash
mkdir my-repository.git
```

3. Navigate into the repository directory:

```bash
cd my-repository.git
```

4. Initialize a bare Git repository:

```bash
git init --bare
```

5. Verify that the repository was created:

```bash
ls -la
```

> Unlike a standard repository, no `.git` directory exists. The repository itself contains all Git metadata.

Example output:

```text
HEAD
branches
config
description
hooks
info
objects
refs
```
