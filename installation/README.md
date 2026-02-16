# Installation

bspwmctl supports multiple Linux distributions. Choose your distribution below for specific instructions.

## Supported Distributions

| Distribution Family | Specific Distros | Status |
|---------------------|------------------|--------|
| Debian | Debian, Ubuntu, Linux Mint, Pop!_OS | ✅ Supported |
| Arch | Arch Linux, Manjaro, EndeavourOS | ✅ Supported |
| Fedora | Fedora, RHEL, CentOS Stream | ✅ Supported |

## Prerequisites

Before installing bspwmctl, make sure you have:

- A working X11 session (Wayland is not supported)
- Git installed
- An internet connection
- Sudo privileges

## Quick Installation

```bash
# Clone the repository
git clone https://github.com/bspwmctl/bspwmctl.git
cd bspwmctl

# Make executable
chmod +x bspwmctl

# Run installation
./bspwmctl install
```

## Distribution-Specific Guides

- [Debian/Ubuntu Installation](installation/debian.md)
- [Arch/Manjaro Installation](installation/arch.md)
- [Fedora Installation](installation/fedora.md)

## What Gets Installed?

Depending on the installation mode you choose:

### Minimal Mode (default)
- bspwm
- sxhkd
- kitty terminal

### Standard Mode
- Everything from Minimal
- Polybar
- Picom
- Rofi

### Full Mode *(coming soon)*
- Everything from Standard
- Zsh + Powerlevel10k
- Additional applications

## Next Steps

After installation, check out the [Usage Guide](usage/) to learn how to use your new bspwm environment.
