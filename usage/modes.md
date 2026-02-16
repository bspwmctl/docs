# Installation Modes

bspwmctl offers different installation modes to suit your needs.

## Available Modes

### Minimal Mode (Default)

**Command:** `./bspwmctl install --minimal` or `./bspwmctl install`

The lightest installation with just the essentials.

**Includes:**
- **bspwm** - Window manager
- **sxhkd** - Hotkey daemon
- **kitty** - Terminal emulator

**Best for:**
- Low-resource systems
- Users who want to customize everything themselves
- Minimalist setups

**Disk space:** ~50MB after compilation

---

### Standard Mode

**Command:** `./bspwmctl install --standard`

Balanced installation with commonly used components.

**Includes:**
- Everything from Minimal mode
- **Polybar** - Status bar
- **Picom** - Compositor (transparency, shadows)
- **Rofi** - Application launcher

**Best for:**
- Most users
- Daily driver setups
- First-time bspwm users

**Disk space:** ~150MB after compilation

---

### Full Mode *(Coming in v0.2.0)*

**Command:** `./bspwmctl install --full`

Complete installation with all the bells and whistles.

**Will include:**
- Everything from Standard mode
- **Zsh** + **Powerlevel10k** - Modern shell
- **Dunst** - Notification daemon
- **Feh** - Wallpaper setter
- Additional utilities and scripts

**Best for:**
- Users who want everything preconfigured
- Complete desktop replacement
- Power users

**Estimated disk space:** ~300MB after compilation

---

## Mode Comparison

| Feature | Minimal | Standard | Full |
|---------|---------|----------|------|
| bspwm + sxhkd | ✅ | ✅ | ✅ |
| Terminal (kitty) | ✅ | ✅ | ✅ |
| Status bar (Polybar) | ❌ | ✅ | ✅ |
| Compositor (Picom) | ❌ | ✅ | ✅ |
| Launcher (Rofi) | ❌ | ✅ | ✅ |
| Zsh + P10k | ❌ | ❌ | ✅ |
| Notifications | ❌ | ❌ | ✅ |
| Extra utilities | ❌ | ❌ | ✅ |
| **Disk Space** | ~50MB | ~150MB | ~300MB |
| **Install Time** | ~5-10 min | ~10-15 min | ~15-20 min |

---

## Switching Between Modes

You can upgrade from one mode to another by running the installer again:

```bash
# Upgrade from minimal to standard
./bspwmctl install --standard

# Upgrade from standard to full (when available)
./bspwmctl install --full
```

The installer will only install missing components.

---

## Which Mode Should I Choose?

### Choose **Minimal** if you:
- Have limited disk space
- Want maximum control over your config
- Are comfortable building your setup from scratch
- Have an older/slower computer

### Choose **Standard** if you:
- Want a good balance of features and simplicity
- Are new to bspwm
- Want something that "just works"
- **← Recommended for most users**

### Choose **Full** if you:
- Want the complete experience
- Don't mind the extra disk space
- Want all tools preconfigured
- Are setting up a new system from scratch

---

## Next Steps

After choosing your mode:

1. [Install bspwmctl](installation/)
2. [Learn the basics](usage/)
3. [Customize your setup](usage/#customization)
