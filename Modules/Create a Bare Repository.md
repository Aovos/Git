# Create a Bare Repository

> A bare repository contains only Git metadata and does not include a working directory.
>
> Bare repositories are commonly used as central remote repositories on servers.

1. Navigate to the directory where you want to create your bare repository:

    ```bash
    cd /path/to/directory
    ```

2. Initialize a bare Git repository:

    ```bash
    git init --bare
    ```

3. Verify that the repository was created:

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

> Most users only need a standard repository. Bare repositories are primarily used as remote repositories on servers.
