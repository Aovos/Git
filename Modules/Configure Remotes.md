# Configure Remotes

> A remote is a reference to a repository hosted on another system, such as GitHub.
>
> Remotes allow you to synchronize changes between your local repository and remote repositories.

## Add a Remote Repository

> `origin` is the conventional name for the primary remote repository.

1. Add a remote repository:

```bash
git remote add origin URL
```

Example:

```bash
git remote add origin https://github.com/USERNAME/REPOSITORY.git
```

## View Configured Remotes

1. Display all configured remotes:

```bash
git remote -v
```

Example output:

```text
origin  https://github.com/USERNAME/REPOSITORY.git (fetch)
origin  https://github.com/USERNAME/REPOSITORY.git (push)
```

## Change a Remote URL

1. Update the URL of an existing remote:

```bash
git remote set-url origin URL
```

Example:

```bash
git remote set-url origin https://github.com/USERNAME/NEW-REPOSITORY.git
```

2. Verify the updated configuration:

```bash
git remote -v
```

## Change the Push URL

> By default, Git uses the same URL for fetching and pushing changes.
>
> A separate push URL can be useful when you want to fetch changes from one repository but push changes to another repository, such as when working with forks.

1. Update only the push URL of an existing remote:

```bash
git remote set-url --push origin URL
```

Example:

```bash
git remote set-url --push origin https://github.com/USERNAME/FORK.git
```

2. Verify the updated configuration:

```bash
git remote -v
```

Example output:

```text
origin  https://github.com/ORIGINAL/REPOSITORY.git (fetch)
origin  https://github.com/USERNAME/FORK.git (push)
```

## Remove a Remote Repository

1. Remove a configured remote:

> Removing a remote only removes the local connection. It does not delete the remote repository.

```bash
git remote remove origin
```
