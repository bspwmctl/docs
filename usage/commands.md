# Commands Reference

Complete reference of all bspwmctl commands.

## Installation Commands

### install

Install bspwm environment with specified mode.

```bash
./bspwmctl install [MODE]
```

**Modes:**
- `--minimal` - Install bspwm, sxhkd, and kitty (default)
- `--standard` - Install minimal + polybar + picom
- `--full` - Full installation *(coming in v0.2.0)*

**Examples:**

```bash
# Minimal installation (default)
./bspwmctl install
./bspwmctl install --minimal

# Standard installation
./bspwmctl install --standard

# Full installation (not yet available)
./bspwmctl install --full
```

## Utility Commands

### check

Check installation status and dependencies.

```bash
./bspwmctl check
```

Shows:
- Which components are installed
- Missing dependencies
- Configuration file locations

### --help / -h

Display help information.

```bash
./bspwmctl --help
./bspwmctl -h
```

### --version / -v

Show bspwmctl version.

```bash
./bspwmctl --version
./bspwmctl -v
```

## Upcoming Commands *(v0.2.0+)*

These commands are planned for future releases:

### update

Update bspwm and related components.

```bash
./bspwmctl update [COMPONENT]
```

### uninstall

Remove bspwm environment.

```bash
./bspwmctl uninstall
```

### theme

Switch between themes.

```bash
./bspwmctl theme [THEME_NAME]
```

## Exit Codes

| Code | Meaning |
|------|---------|
| `0` | Success |
| `1` | General error |
| `2` | Missing dependencies |
| `3` | Unsupported distribution |
| `130` | User cancelled (Ctrl+C) |

## Examples

### Fresh Installation

```bash
# Clone and install in one go
git clone https://github.com/bspwmctl/bspwmctl.git && \
cd bspwmctl && \
chmod +x bspwmctl && \
./bspwmctl install --standard
```

### Check Before Installing

```bash
# Check if your system is compatible
./bspwmctl check

# Then install if everything looks good
./bspwmctl install
```

## Getting Help

If you encounter issues with any command:

1. Check the [Troubleshooting Guide](installation/#troubleshooting)
2. Run `./bspwmctl check` to diagnose
3. [Open an issue](https://github.com/bspwmctl/bspwmctl/issues/new/choose)
