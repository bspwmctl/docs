# Installation modes

Each mode includes everything from the previous one.

## Minimal (default)

```bash
bspwmctl install
```

Just what you need to use bspwm:

- **bspwm**: window manager
- **sxhkd**: keybindings
- **kitty**: terminal
- **rofi**: app launcher
- **feh**: wallpaper and image viewer

Best for users who want to build their own setup on top.

## Standard (recommended)

```bash
bspwmctl install --standard
```

A complete desktop:

- **Polybar**: status bar
- **Picom**: compositor (transparency, shadows)
- **Dunst**: notifications
- **i3lock**: lock screen
- **Flameshot**: screenshots
- **Volume and brightness keys**: `pactl`, `brightnessctl`, and **pavucontrol** to manage audio
- **Polkit agent**: lets graphical apps ask for your password
- **xclip**: clipboard tool, **Papirus** icons
- **Zsh** with autosuggestions and syntax highlighting

?> Standard mode makes **zsh your default shell** and installs its own `~/.zshrc`. Your previous `~/.zshrc` is [backed up](usage/backups.md).

## Full

```bash
bspwmctl install --all
```

Standard plus everyday apps:

- **Thunar**: file manager (`super + e`)
- **Firefox**: browser (`super + shift + f`). Firefox ESR on Debian; Ubuntu-based distros keep their own Firefox.
- **btop**: system monitor
- **mpv**: video player
- **zathura**: PDF viewer
- **NetworkManager connection editor**

## Changing mode

Run `bspwmctl install` again with another mode. Packages you already have are skipped, so moving up from minimal to standard only installs what is missing.

Moving down doesn't uninstall anything: packages from a bigger mode stay installed.
