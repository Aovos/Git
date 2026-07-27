# Git

[Installation](#installation)

[Git Identity](#git-identity)


## Installation
```bash
git --version
```
> If a version number is displayed, you are ready to proceed
> > otherwise, you must install Git first.


### Debian

```bash
sudo apt update
sudo apt install git
```

### NixOS

> Go to your NixOS configuration: `/etc/nixos/configuration.nix`:
> > Paste `git` inside the `systemPackages`
```nix
environment.systemPackages = with pkgs; [
  git
];
```

> After that, rebuild your NixOS system and switch to it:
```bash
sudo nixos-rebuild switch
```


## Git Identity

### Global Identity Configuration

> Applies to all repositories by default.
> > Set your global `username` and `e-mail`:
```bash
git config --global user.name "Your Name"
git config --global user.email "Your e-mail"
```
> Check the global identity configuration
```bash
git config --global user.name
git config --global user.email
```

### Local Identity Configuration
> Applies only to the current repository and overrides the global configuration.
> > Navigate to your repository
```bash
cd your-repository
```

> Set your local `username` and `e-mail`:
```bash
git config user.name "Your Name"
git config user.email "Your e-mail"
```

> Check the local identity configuration
```bash
git config user.name
git config user.email
```



