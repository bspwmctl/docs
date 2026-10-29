# Installation

## Supported distributions

| Family | Tested on | Should also work on |
|--------|-----------|---------------------|
| Debian | Debian 13, Ubuntu 24.04 | Kali, Parrot, Linux Mint, Pop!_OS... |
| Arch | Arch Linux | Manjaro, EndeavourOS, Garuda... |
| Fedora | Fedora | Nobara... |

Derivatives are detected automatically. bspwmctl prints a warning when your distro hasn't been tested, but it will use the packages of its family. RHEL, CentOS, Rocky and AlmaLinux are **not** supported: bspwm is not in their repositories.

## Requirements

- A normal user with `sudo` privileges
- An internet connection
- A login screen (display manager) that can start **X11** sessions. bspwm does not run on Wayland.

## Install bspwmctl

### Option 1: package (recommended)

Download the package for your distro from the [latest release](https://github.com/bspwmctl/bspwmctl/releases) and install it with your package manager. The guide for your distro has the exact commands:

- [Debian / Ubuntu](installation/debian.md)
- [Arch / Manjaro](installation/arch.md)
- [Fedora](installation/fedora.md)

The package installs the `bspwmctl` command, so it is available from anywhere.

### Option 2: from the repository

```bash
git clone https://github.com/bspwmctl/bspwmctl.git
cd bspwmctl
./bspwmctl install
```

Use this if you want to try the latest changes or contribute.

## Install the desktop

Once bspwmctl is installed, run it **as your normal user** (not with `sudo`; it will ask for your password when it needs it):

```bash
bspwmctl install              # minimal: bspwm, sxhkd, kitty, rofi
bspwmctl install --standard   # + bar, compositor, notifications, zsh... (recommended)
bspwmctl install --all        # + file manager, browser and other apps
```

See [Installation modes](usage/modes.md) for the full list of what each mode installs.

bspwmctl will:

1. Detect your distribution
2. Install the packages with `apt`, `pacman` or `dnf`
3. Back up any config it is about to overwrite (see [Backups](usage/backups.md))
4. Copy its configs to `~/.config/` and install the bundled fonts

Then log out, choose **bspwm** in your login screen and log back in.

## Update and uninstall

```bash
bspwmctl update       # install the latest version of bspwmctl
bspwmctl uninstall    # remove its configs and restore yours
```

See [Commands](usage/commands.md#update) for details.

## Troubleshooting

### bspwm doesn't appear in the login screen

The bspwm package installs a session file in `/usr/share/xsessions/`. If your login screen still doesn't list it, it probably only supports Wayland sessions. Install a display manager that supports X11, such as LightDM.

### Warning about `/usr/local/bin`

bspwmctl 0.1.0 compiled bspwm, sxhkd, polybar and picom from source into `/usr/local/bin`. Those binaries take precedence over the packages, and bspwmctl warns about each one it finds. Delete them to use the packaged versions, for example:

```bash
sudo rm /usr/local/bin/bspwm /usr/local/bin/bspc
```
