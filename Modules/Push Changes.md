# Push Changes

> Pushing uploads local commits to a remote repository.
>
> This allows other users to access your changes and keeps the remote repository up to date.

## Push Changes

Push changes to the remote repository:

```bash
git push
```

> Git pushes commits to the configured upstream branch.

## Push to a Specific Branch

Push changes to a specific remote branch:

```bash
git push origin main
```

> Replace `main` with the name of the branch you want to push.

## Upstream Branch

> An upstream branch is the default remote branch that a local branch is linked to.
>
> Once configured, Git knows where to push changes and where to pull changes from without requiring the remote and branch name every time.
>
> Simplified, an upstream branch works like an alias. Git remembers the default remote and branch so you can use shorter commands.

Example:

```text
Local Branch:  main
Remote Branch: origin/main
```

After the upstream branch has been configured, the following commands can usually be used:

```bash
git push
git pull
```

Instead of:

```bash
git push origin main
git pull origin main
```

## Set an Upstream Branch

> When pushing a branch for the first time, Git can store a default remote and branch for future push and pull operations.

1. Push the branch and set the upstream branch:

```bash
git push -u origin main
```
<
> The `-u` option tells Git to use `origin/main` as the default remote branch for the local `main` branch.
>
> After the upstream branch has been configured, future pushes and pulls can usually be performed using:

```bash
git push
git pull
```

Instead of:

```bash
git push origin main
git pull origin main
```

## Change the Upstream Branch

> If you want to use a different remote or branch as the default target, run the command again with the desired values.

Example:

```bash
git push -u origin develop
```

> This updates the default upstream branch for the current local branch.

## Verify the Upstream Branch

1. Display information about the current branch:

```bash
git branch -vv
```

Example output:

```text
* main abc1234 [origin/main] Add repository documentation
```

> The value shown in brackets indicates the configured upstream branch.

## Verify the Push

1. Display the repository status:

```bash
git status
```

Example output:

```text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```
