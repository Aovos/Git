# Connect Local Repo to GitHub

### 1. [Configure Remotes.md](../Modules/Configure%20Remotes.md)

Connect the local repository to a GitHub repository:

```bash
git remote add origin https://github.com/USERNAME/REPOSITORY.git
```

### 2. [Push Changes](../Modules/Push%20Changes.md)

Push the local branch and configure the upstream branch:

```bash
git push -u origin main
```

### 3. [Authenticate with GitHub using HTTPS](../Modules/Authenticate%20with%20GitHub%20using%20HTTPS%20(Terminal.md))

If GitHub requests authentication during the push operation, authenticate using your GitHub username and Personal Access Token (PAT).

### Result
You now have:

- A local repository connected to GitHub
- A configured remote named `origin`
- A configured upstream branch
- Local commits published to GitHub
