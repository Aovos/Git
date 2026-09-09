# Git Identity

> Git Identity defines the author information that is attached to your commits. Each commit stores a username and e-mail address, allowing Git to identify who created the changes.
>
> > Git requires a configured identity before commits can be created!

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
>
> Local configuration takes precedence over global configuration for the current repository.

1. Navigate to your repository:

```bash
cd /path/to/repository
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

## Update an Identity

> Running the configuration command again with different values updates the existing identity.

Update the Global Identity

```bash
git config --global user.name "New Name"
git config --global user.email "new@example.com"
```

Update the Local Identity

```bash
git config user.name "New Name"
git config user.email "new@example.com"
```

## Remove an Identity

Remove the Global Identity

```bash
git config --global --unset user.name
git config --global --unset user.email
```

Remove the Local Identity

```bash
git config --unset user.name
git config --unset user.email
```
