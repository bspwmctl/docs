# Arch/Manjaro Installation

This guide covers installing bspwmctl on Arch-based distributions including Arch Linux, Manjaro, and EndeavourOS.

## Prerequisites

Update your system:

```bash
sudo pacman -Syu
```

Install Git and base development tools:

```bash
sudo pacman -S git base-devel
```

## Installation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/bspwmctl/bspwmctl.git
cd bspwmctl
```

### 2. Make Executable

```bash
chmod +x bspwmctl
```

### 3. Run Installer

Choose your installation mode:

**Minimal (bspwm + sxhkd + kitty):**
```bash
./bspwmctl install --minimal
```

**Standard (includes Polybar and Picom):**
```bash
./bspwmctl install --standard
```

### 4. Log Out and Select bspwm

After installation:

1. Log out
2. Select **bspwm** from your display manager
3. Log back in

## Dependencies

bspwmctl installs these from official repos:

```
base-devel
libxcb
xcb-util
xcb-util-wm
xcb-util-keysyms
xcb-util-cursor
```

## Using AUR Packages (Optional)

Some users prefer AUR packages. If you want to use those instead:

```bash
# Example with yay
yay -S bspwm-git sxhkd-git
```

However, bspwmctl compiles from source by default for the latest features.

## Troubleshooting

### Package Conflicts

If you have existing bspwm packages:

```bash
sudo pacman -R bspwm sxhkd
```

Then run bspwmctl again.

## Next Steps

- [Basic Usage](usage/)
- [Available Commands](usage/commands.md)
