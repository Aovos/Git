# Git-Installation

1. Check if Git is already installed on your system:

```bash
git --version
```

> If a version number is displayed, Git is already installed. Otherwise, follow the installation instructions below.

## Debian

2. Install Git using the Debian package manager:

```bash
sudo apt update
sudo apt install git
```

## NixOS

2. Open your NixOS configuration file:

```text
/etc/nixos/configuration.nix
```

3. Add `git` to `environment.systemPackages`:

```nix
environment.systemPackages = with pkgs; [
  git
];
```

4. Rebuild your NixOS system and switch to the new configuration:

```bash
sudo nixos-rebuild switch
```
