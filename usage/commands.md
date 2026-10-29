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

## update

```bash
bspwmctl update              # update bspwmctl to the latest version
bspwmctl update --configs    # and re-apply the new default configs
```

Downloads the package of the latest release from GitHub and installs it with `apt`, `dnf` or `pacman`. If you are on a beta, you get the newest beta or release; on a stable version, only stable releases.

Your configs are not changed unless you add `--configs`. Then the configs of your current theme are applied again, with your current ones backed up first (see [Backups](usage/backups.md)).

?> If you run bspwmctl from a clone of the repository, update it with `git pull` instead.

## uninstall

```bash
bspwmctl uninstall           # asks for confirmation
bspwmctl uninstall --yes     # doesn't ask
```

Removes what bspwmctl wrote to your home folder and puts back what you had before:

- `~/.config/bspwm`, `sxhkd`, `kitty`, `polybar`, `picom`, `dunst` and `~/.zshrc`: removed, or replaced by the version you had before installing bspwmctl
- The bundled fonts in `~/.local/share/fonts/bspwmctl/`
- Your login shell goes back to the one you had before, if bspwmctl changed it to zsh

Everything it removes is backed up first, so you can get it back with `bspwmctl restore`. The installed programs (bspwm, kitty, polybar...) are kept. To remove bspwmctl itself afterwards:

```bash
sudo apt remove bspwmctl      # Debian / Ubuntu
sudo pacman -R bspwmctl       # Arch
sudo dnf remove bspwmctl      # Fedora
```

!> If you installed with 0.2.0-beta.1, bspwmctl doesn't know which configs you had before, so it removes all of them. You can still find your old ones in the backups.

## help / version

```bash
bspwmctl help        # or -h, --help
bspwmctl version     # or -v, --version
```

## Exit codes

| Code | Meaning |
|------|---------|
| `0` | Success |
| `1` | Error (the message explains why) |
| `130` | Cancelled with Ctrl+C |
