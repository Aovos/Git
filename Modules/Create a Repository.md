# Create a Repository

> A Git repository stores your project's files, history, branches, and metadata.
>
> Git provides two repository types: standard repositories and bare repositories.

## Standard Repository

> A standard repository contains both your working directory and the Git metadata in the same location.

1. Navigate to the directory where you want to create your repository:

    ```bash
    cd ~/Projects/MyProject
    ```

2. Initialize a standard Git repository:

    ```bash
    git init
    ```

    Example output:

    ```text
    Initialized empty Git repository in /path/to/project/.git/
    ```

> Git creates a hidden `.git` directory inside your current working directory. This directory contains all repository metadata.

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
