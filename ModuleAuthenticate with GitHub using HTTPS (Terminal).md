# Authenticate with GitHub using HTTPS (Terminal)

> GitHub requires authentication before changes can be pushed to a remote repository on GitHub.
>
> This module covers HTTPS authentication when using Git from the terminal.
>
> When using HTTPS, GitHub no longer accepts account passwords for Git operations. Instead, a Personal Access Token (PAT) must be used.
>
> Make sure your Git identity matches the GitHub account used to access the remote repository!

## Create a Personal Access Token

1. Sign in to GitHub.

2. Open:

```text
Settings
→ Developer Settings
→ Personal Access Tokens
→ Tokens (Classic)
```

3. Create a new token.

4. Select the required permissions.

5. Generate the token.

> Copy and store the token in a secure location.
>
> GitHub only displays the token once!!!

## Authenticate During a Push

1. Push your changes:

```bash
git push -u origin main
```

2. Enter your GitHub username when prompted:

```text
Username: YOUR_USERNAME
```

3. Enter your Personal Access Token when prompted for a password:

```text
Password: YOUR_PERSONAL_ACCESS_TOKEN
```

## Configure Credential Storage

> Git can store your authentication credentials to avoid repeatedly entering your username and Personal Access Token.
>
> Different credential helpers provide different storage methods.

### Git Credential Manager (Recommended)

> Stores credentials securely using the operating system's credential manager.

Configure Git Credential Manager:

```bash
git config --global credential.helper manager
```

Verify the configuration:

```bash
git config --global credential.helper
```

Example output:

```text
manager
```

### Store Credentials in a File

> Stores credentials in plain text on disk.
>
> This method is less secure and should only be used when a credential manager is unavailable.

Configure credential storage:

```bash
git config --global credential.helper store
```

Verify the configuration:

```bash
git config --global credential.helper
```

Example output:

```text
store
```

> After a successful authentication, Git stores your credentials and automatically reuses them for future Git operations.
