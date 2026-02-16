# Fedora Installation

This guide covers installing bspwmctl on Fedora and RHEL-based distributions.

## Prerequisites

Update your system:

```bash
sudo dnf update -y
```

Install development tools:

```bash
sudo dnf groupinstall "Development Tools" -y
sudo dnf install git -y
```

## Installation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/bspwmctl/bspwmctl.git
cd bspwmctl
```

### 2. Make Executable

```bash
chmod +x bspwmctl
```

### 3. Run Installer

Choose your installation mode:

**Minimal (bspwm + sxhkd + kitty):**
```bash
./bspwmctl install --minimal
```

**Standard (includes Polybar and Picom):**
```bash
./bspwmctl install --standard
```

### 4. Log Out and Select bspwm

After installation:

1. Log out of your session
2. Select **bspwm** from GDM/SDDM
3. Log in

## Dependencies

bspwmctl will install these RPM packages:

```
gcc
make
libxcb-devel
xcb-util-devel
xcb-util-wm-devel
xcb-util-keysyms-devel
xcb-util-cursor-devel
```

## Troubleshooting

### SELinux Issues

If you encounter permission errors, you may need to temporarily set SELinux to permissive:

```bash
sudo setenforce 0
```

Run the installer, then re-enable:

```bash
sudo setenforce 1
```

### Missing Dependencies

Install development headers:

```bash
sudo dnf install libX11-devel libXft-devel
```

## Next Steps

- [Basic Usage](usage/)
- [Available Commands](usage/commands.md)
