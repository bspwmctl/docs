# Keybindings

`super` is the Windows key. All keybindings live in `~/.config/sxhkd/sxhkdrc`; after editing it, reload with `super + Escape`.

## Apps

| Keys | Action |
|------|--------|
| `super + Return` | Terminal (kitty) |
| `super + d` | App launcher (rofi) |
| `super + e` | File manager (Thunar, `--all`) |
| `super + shift + f` | Browser (Firefox, `--all`) |
| `super + l` | Lock screen |
| `Print` | Screenshot of an area |
| `shift + Print` | Screenshot of the whole screen |

## Windows

| Keys | Action |
|------|--------|
| `super + w` | Close window |
| `super + shift + w` | Kill window |
| `super + ←↓↑→` | Focus window in that direction |
| `super + shift + ←↓↑→` | Swap with the window in that direction |
| `super + alt + ←↓↑→` | Resize window |
| `super + ctrl + ←↓↑→` | Move floating window |
| `super + t` | Tiled |
| `super + shift + t` | Pseudo-tiled |
| `super + s` | Floating |
| `super + f` | Fullscreen |
| `super + m` | Toggle monocle layout (one window fills the desktop) |
| `super + g` | Swap with the biggest window |

## Desktops

| Keys | Action |
|------|--------|
| `super + 1` ... `super + 0` | Go to desktop 1-10 |
| `super + shift + 1` ... `super + shift + 0` | Send window to desktop 1-10 |
| `super + [` / `super + ]` | Previous / next desktop |
| `super + Tab` | Last desktop |
| `super + `` ` `` | Last window |

## Preselection

Choose where the next window will open:

| Keys | Action |
|------|--------|
| `super + ctrl + alt + ←↓↑→` | Preselect a direction |
| `super + ctrl + 1` ... `9` | Preselect the size (10%-90%) |
| `super + ctrl + space` | Cancel preselection |

## Media

| Keys | Action |
|------|--------|
| Volume keys | Volume up / down / mute |
| Brightness keys | Brightness up / down |

## Session

| Keys | Action |
|------|--------|
| `super + Escape` | Reload keybindings |
| `super + alt + r` | Restart bspwm |
| `super + alt + q` | Log out |
