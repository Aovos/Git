# Git Identity

> Git Identity defines the author information that is attached to your commits. Each commit stores a username and e-mail address, allowing Git to identify who created the changes.

## Global Identity Configuration

> Applies to all repositories for the current user.
1. Set your global username and e-mail address:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

2. Check the global identity configuration:

```bash
git config --global user.name
git config --global user.email
```
> The output should display the values you previously configured.
Example output:
```text
Your Name
you@example.com
```

## Local Identity Configuration

> Applies only to the current repository and overrides the global configuration. Useful when a specific repository requires a different identity than your global configuration.

1. Navigate to your repository:

```bash
cd ~/Projects/my-project
```

2. Set your local username and e-mail address:

```bash
git config user.name "Your Name"
git config user.email "you@example.com"
```

3. Check the local identity configuration:

```bash
git config user.name
git config user.email
```

> The output should display the values you previously configured.

Example output:

```text
Your Name
you@example.com
```

> Local configuration always takes precedence over global configuration!
