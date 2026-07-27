# Ignoring Files

> Sometimes files or directories should not be tracked by Git.
> > Common examples include log files, temporary files, build artifacts, and files containing sensitive information.
> > Git uses a `.gitignore` file to define which files and directories should be ignored.

## Create a .gitignore File

1. Create a `.gitignore` file in the root directory of your repository:

```bash
touch .gitignore
```

## Ignore Specific Files

1. Ignore a specific file:

```gitignore
secret.txt
```

> Git will ignore any file named `secret.txt`.

## Ignore File Types

1. Ignore all files of a specific type:

```gitignore
*.log
*.tmp
```

> This example ignores all `.log` and `.tmp` files.

## Ignore Directories

1. Ignore an entire directory:

```gitignore
node_modules/
build/
dist/
```

> All files and subdirectories inside those directories will be ignored.

## Verify Ignored Files

1. Check the repository status:

```bash
git status
```

> Ignored files will not appear in the output.

## Already Tracked Files

> The file will remain on disk, but Git will no longer track it.

1. Remove the file from the Git index while keeping it on disk.

```bash
git rm --cached secret.txt
```

2. Add the file to `.gitignore`.

3. Create a new commit.

> The file will remain on disk, but Git will no longer track it.
