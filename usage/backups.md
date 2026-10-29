# Backups

bspwmctl never overwrites your files without keeping a copy.

## How it works

Before `bspwmctl install`, `theme`, `update --configs` or `uninstall` replaces or removes a config, it checks whether any of your files would change. If so, it copies them to:

```
~/.local/share/bspwmctl/backups/<date>/
```

Each run gets its own folder, named after the date and time (for example `20261025-182829`). Running the same command again without changes doesn't create a new backup.

This covers everything bspwmctl writes: `~/.config/bspwm`, `sxhkd`, `kitty`, `polybar`, `picom`, `dunst` and `~/.zshrc`.

## Restoring

List your backups:

```bash
bspwmctl restore
```

```
[*] Available backups (newest last):
  20261025-182829  bspwm kitty .zshrc
```

Restore one:

```bash
bspwmctl restore 20261025-182829
```

Restoring is safe too: your current configs are backed up first, so you can undo a restore with another `bspwmctl restore`.

?> Backups are not deleted automatically. You can remove old ones by deleting their folders in `~/.local/share/bspwmctl/backups/`.
