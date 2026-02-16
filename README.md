# bspwmctl

[![Version](https://img.shields.io/badge/version-v0.1.0-blue.svg)](https://github.com/bspwmctl/bspwmctl)
[![Status](https://img.shields.io/badge/status-Pre--Alpha-red.svg)]()
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

**bspwmctl** is an automated installer and manager designed to deploy a fully configured bspwm desktop environment without the manual hassle.

!> **WARNING: PRE-ALPHA SOFTWARE**<br>
This version (v0.1.0) is a **Pre-Alpha** release. It is intended for testing purposes on fresh installations.<br>

---


## 🧩 What is bspwm?

For those new to the ecosystem, **bspwm** (Binary Space Partitioning Window Manager) is a tiling window manager for X11.

Unlike traditional desktop environments (like GNOME or KDE), bspwm:
* **Tiles windows automatically:** Instead of overlapping windows, it splits the screen so you can see everything at once.
* **Is extremely lightweight:** Uses minimal RAM and CPU resources.
* **Is controlled by scripts:** Its configuration is handled by a simple shell script, making it incredibly hackable and flexible.

**bspwmctl** bridges the gap between a fresh Linux install and a fully functional, beautiful bspwm environment.


## ✨ Features (v0.1.0)

- 🐧 **Multi-distribution support**: Currently testing on Debian, Arch, and Fedora.
- 📦 **Smart Installation**: Detects your package manager and installs dependencies automatically.
- 🎨 **Dotfiles Injection**: Deploys pre-configured setups for:
  - `bspwm` (Window Manager)
  - `sxhkd` (Hotkeys)
  - `polybar` (Status bar)
  - `picom` (Compositor/Transparency)
  - `kitty` (Terminal emulator)
- 🚀 **CLI Based**: Simple command-line interface (future versions will include a compiled binary).


## 🚀 Quick Start

Remember: **Do not use sudo**.

```bash
# 1. Clone the repository
git clone [https://github.com/bspwmctl/bspwmctl.git](https://github.com/bspwmctl/bspwmctl.git)
cd bspwmctl

# 2. Make the script executable
chmod +x bspwmctl

# 3. Install (Default / Minimal mode)
./bspwmctl install

# Option: Install with standard packages
./bspwmctl install --standard
```


## Next Steps

- 📖 [Installation Guide](installation/) - Detailed installation instructions

- 🎯 [Usage Guide](usage/) - Learn how to use bspwmctl

- 🤝 [Contributing](contributing/) - Help improve bspwmctl


## 🤝 Contributing

Found a bug? Want to add support for your distro?
Check out the [Contributing Guide](contributing/README.md) or open an [Issues](https://github.com/bspwmctl/bspwmctl/issues).


## 📄 License

bspwmctl is released under the [MIT License](https://github.com/bspwmctl/bspwmctl/blob/main/LICENSE).
