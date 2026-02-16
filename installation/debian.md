# Debian/Ubuntu Installation

This guide covers installing bspwmctl on Debian-based distributions including Ubuntu, Linux Mint, and Pop!_OS.

## Prerequisites

Update your system first:

```bash
sudo apt update
sudo apt upgrade -y
```

Install Git if you don't have it:

```bash
sudo apt install git -y
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

After installation completes:

1. Log out of your current session
2. At the login screen, select **bspwm** from the session menu
3. Log back in

## Dependencies

bspwmctl will automatically install these dependencies:

```
build-essential
libxcb-util-dev
libxcb-ewmh-dev
libxcb-randr0-dev
libxcb-icccm4-dev
libxcb-keysyms1-dev
libxcb-xinerama0-dev
xcb
libxcb-cursor-dev
```

Plus application-specific dependencies for kitty, polybar, etc.

## Troubleshooting

### Build Fails

If compilation fails, make sure you have all development tools:

```bash
sudo apt install build-essential pkg-config -y
```

### Missing Dependencies

Run the dependency check:

```bash
./bspwmctl check
```

## Next Steps

- [Basic Usage](usage/)
- [Available Commands](usage/commands.md)
