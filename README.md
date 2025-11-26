# Dank Linux Packages for Arch Linux

This repository includes a few packages relating to AvengeMedia's [Dank Linux](https://danklinux.com), including dms-shell and various other tools/compositors surrounding it. All PKGBUILDs are listed in the `pkgs/` folder in the repository root.

## Using the repository

In order to install packages from this repository via `pacman`, you need to import the signing key:

```bash
pacman-key --init
pacman-key --recv-key 5DE6BF3EBC86402E7A5C5D241FA48C960F9604CB --keyserver keyserver.ubuntu.com
pacman-key --lsign-key 5DE6BF3EBC86402E7A5C5D241FA48C960F9604CB
```

And add the following to `/etc/pacman.conf`:
```ini
[danklinux]
SigLevel = Required
Server = https://github.com/hecknt/arch-danklinux-pkgs/releases/download/$repo
```

Afterwards, sync your repositories with `pacman -Sy`, and then install a package like so:

```bash
pacman -S dms-shell
```
