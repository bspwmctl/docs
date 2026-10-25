# First steps

## Log in

After `bspwmctl install`, log out, open the session menu in your login screen (usually a gear icon), choose **bspwm** and log in.

## The basics

| Keys | Action |
|------|--------|
| `super + Return` | Open a terminal (kitty) |
| `super + d` | Open the app launcher (rofi) |
| `super + w` | Close the focused window |
| `super + 1` ... `super + 0` | Go to desktop 1-10 |
| `super + alt + q` | Log out of bspwm |

`super` is the Windows key. See [Keybindings](usage/keybindings.md) for the full list.

## Wallpaper

Save an image as `~/.config/bspwm/wallpaper.png` (or `.jpg`) and restart bspwm with `super + alt + r`. Without it, a plain background color is used.

## Your config files

```
~/.config/bspwm/     window manager: desktops, gaps, window rules, autostart
~/.config/sxhkd/     keybindings
~/.config/kitty/     terminal
~/.config/polybar/   status bar      (--standard)
~/.config/picom/     compositor      (--standard)
~/.config/dunst/     notifications   (--standard)
~/.zshrc             shell           (--standard)
```

They are yours to edit. If you run `bspwmctl install` or `bspwmctl theme` again, your changed files are [backed up](usage/backups.md) before being replaced.

## Customize

- **Keybindings:** edit `~/.config/sxhkd/sxhkdrc`, then reload it with `super + Escape`.
- **Window manager:** edit `~/.config/bspwm/bspwmrc`, then restart bspwm with `super + alt + r`.
- **Multiple monitors:** add your `xrandr` setup at the top of `~/.config/bspwm/bspwmrc`.
