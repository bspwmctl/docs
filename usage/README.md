# Basic Usage

Learn how to use bspwmctl after installation.

## Quick Reference

```bash
# Install bspwm environment
./bspwmctl install [--minimal|--standard|--full]

# Check installation status
./bspwmctl check

# Show help
./bspwmctl --help

# Show version
./bspwmctl --version
```

## First Steps After Installation

### 1. Log into bspwm

After running the installer:

1. Log out of your current session
2. At the login screen, click the session selector (usually a gear icon)
3. Select **bspwm**
4. Log in with your credentials

### 2. Basic Keyboard Shortcuts

The default keybindings (configured in `~/.config/sxhkd/sxhkdrc`):

| Shortcut | Action |
|----------|--------|
| `Super + Enter` | Open terminal (kitty) |
| `Super + Space` | Open app launcher (rofi) |
| `Super + w` | Close window |
| `Super + m` | Toggle monocle mode |
| `Super + [1-9]` | Switch to desktop 1-9 |
| `Super + Shift + [1-9]` | Move window to desktop 1-9 |
| `Super + h/j/k/l` | Focus window (left/down/up/right) |
| `Super + Alt + h/j/k/l` | Resize window |
| `Super + Shift + q` | Restart bspwm |
| `Super + Shift + Escape` | Reload sxhkd config |

### 3. Explore Your Config

Your configuration files are located in:

```
~/.config/bspwm/        ← Window manager config
~/.config/sxhkd/        ← Keyboard shortcuts
~/.config/kitty/        ← Terminal config
~/.config/polybar/      ← Status bar (if standard mode)
~/.config/picom/        ← Compositor (if standard mode)
```

## Installation Modes

See [Installation Modes](usage/modes.md) for detailed comparison.

## Available Commands

Check out [Commands Reference](usage/commands.md) for all available commands.

## Customization

### Change Keyboard Shortcuts

Edit `~/.config/sxhkd/sxhkdrc`:

```bash
nano ~/.config/sxhkd/sxhkdrc
```

After editing, reload with `Super + Shift + Escape`

### Modify Window Rules

Edit `~/.config/bspwm/bspwmrc`:

```bash
nano ~/.config/bspwm/bspwmrc
```

Then restart bspwm with `Super + Shift + q`

## Getting Help

- [GitHub Issues](https://github.com/bspwmctl/bspwmctl/issues)
- [Contributing Guide](https://github.com/bspwmctl/bspwmctl/blob/main/CONTRIBUTING.md)
