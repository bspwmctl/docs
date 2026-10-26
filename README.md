# bspwmctl

[![Version](https://img.shields.io/github/v/release/bspwmctl/bspwmctl?include_prereleases&label=version&color=blue)](https://github.com/bspwmctl/bspwmctl/releases)
[![Status](https://img.shields.io/badge/status-Beta-orange.svg)](https://github.com/bspwmctl/bspwmctl/releases)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](https://github.com/bspwmctl/bspwmctl/blob/main/LICENSE)

**bspwmctl** installs and manages a fully configured bspwm desktop: window manager, hotkeys, status bar, compositor, notifications and more, ready to use after a single command.

!> **Beta software.** v0.2.0 is still in testing. Your existing configs are backed up before anything is overwritten, but try it on a test machine or VM first if you can.

## 🧩 What is bspwm?

[bspwm](https://github.com/baskerville/bspwm) is a **tiling window manager** for X11. Unlike desktops such as GNOME or KDE:

- **It tiles windows automatically**: instead of overlapping, windows split the screen so you see everything at once.
- **It is very lightweight**: it uses little RAM and CPU.
- **It is configured with shell scripts**: easy to read, hack and extend.

Setting up bspwm by hand takes a lot of pieces (hotkey daemon, bar, compositor, launcher, notifications...). bspwmctl installs and configures all of them for you.

## ✨ Features

- 📦 **Official packages only**: everything is installed with `apt`, `pacman` or `dnf`, so it is updated and removed like any other package. Nothing is compiled.
- 🐧 **Multi-distro**: Debian, Ubuntu, Arch, Fedora and their derivatives.
- 🧱 **Three modes**: [minimal, standard and full](usage/modes.md), from just the window manager to a complete desktop.
- 🎨 **Ready-to-use configs** for bspwm, sxhkd, kitty, polybar, picom, dunst and zsh.
- 💾 **Automatic [backups](usage/backups.md)** of any config it would overwrite, with `bspwmctl restore` to go back.

## 🚀 Quick Start

Download the package for your distro from the [latest release](https://github.com/bspwmctl/bspwmctl/releases) and install it:

```bash
# Debian / Ubuntu
sudo apt install ./bspwmctl_*_all.deb

# Fedora
sudo dnf install ./bspwmctl-*.noarch.rpm

# Arch
sudo pacman -U ./bspwmctl-*-any.pkg.tar.zst
```

Then, **as your normal user** (not with `sudo`):

```bash
bspwmctl install --standard
```

Log out, choose **bspwm** in your login screen and log back in. See [First steps](usage/) for what to do next.

## Next Steps

- 📖 [Installation guide](installation/): all installation methods and supported distros
- 🧱 [Installation modes](usage/modes.md): what each mode installs
- ⌨️ [Keybindings](usage/keybindings.md): how to use your new desktop
- 🤝 [Contributing](contributing/): help improve bspwmctl

## 📄 License

bspwmctl is released under the [MIT License](https://github.com/bspwmctl/bspwmctl/blob/main/LICENSE).
