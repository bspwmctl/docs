# Arch / Manjaro

This guide covers Arch Linux and its derivatives (Manjaro, EndeavourOS, Garuda...).

## 1. Install bspwmctl

Download the `.pkg.tar.zst` from the [latest release](https://github.com/bspwmctl/bspwmctl/releases) and install it:

```bash
sudo pacman -U ./bspwmctl-*-any.pkg.tar.zst
```

## 2. Install the desktop

As your normal user:

```bash
bspwmctl install --standard
```

## 3. Log in to bspwm

Log out, choose **bspwm** in the session menu of your login screen and log back in.

## Notes

- **Full system upgrade:** bspwmctl installs packages with `pacman -Syu`, which also upgrades the rest of your system. Arch doesn't support partial upgrades, so this avoids broken dependencies.
- **No AUR needed:** everything bspwmctl installs comes from the official repositories.
- **Garuda and other derivatives** are not tested yet. They should work, and bspwmctl will warn you about it. Please [report](https://github.com/bspwmctl/bspwmctl/issues) any problem.
