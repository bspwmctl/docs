# Commands

Run every command as your normal user, not with `sudo`.

## install

Install the desktop and apply the default configs.

```bash
bspwmctl install [--minimal | --standard | --all] [--no-dep] [--theme <name>]
```

| Option | Description |
|--------|-------------|
| `--minimal` | bspwm, sxhkd, kitty, rofi (default) |
| `--standard` | + bar, compositor, notifications, lock screen, zsh... |
| `--all` | + file manager, browser and other apps |
| `--no-dep` | Don't install packages, only apply the configs |
| `--theme <name>` | Theme to apply (default: `default`) |

See [Installation modes](usage/modes.md) for details.

## theme

```bash
bspwmctl theme            # show the current theme and the available ones
bspwmctl theme <name>     # apply a theme
```

For now there is only the `default` theme. More themes will come from the [themes repository](https://github.com/bspwmctl/themes).

## restore

```bash
bspwmctl restore             # list backups
bspwmctl restore <backup>    # restore one
```

See [Backups](usage/backups.md).

## help / version

```bash
bspwmctl help        # or -h, --help
bspwmctl version     # or -v, --version
```

## Coming soon

- `bspwmctl update`
- `bspwmctl uninstall`

Until `uninstall` is available, remove bspwmctl with your package manager (`sudo apt remove bspwmctl`, `sudo pacman -R bspwmctl` or `sudo dnf remove bspwmctl`). The desktop packages are normal packages and can be removed the same way.

## Exit codes

| Code | Meaning |
|------|---------|
| `0` | Success |
| `1` | Error (the message explains why) |
| `130` | Cancelled with Ctrl+C |
