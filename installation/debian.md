# Debian / Ubuntu

This guide covers Debian, Ubuntu and their derivatives (Kali, Parrot, Linux Mint, Pop!_OS...).

## 1. Install bspwmctl

Download the `.deb` from the [latest release](https://github.com/bspwmctl/bspwmctl/releases) and install it:

```bash
sudo apt install ./bspwmctl_*_all.deb
```

## 2. Install the desktop

As your normal user:

```bash
bspwmctl install --standard
```

## 3. Log in to bspwm

Log out, choose **bspwm** in the session menu of your login screen and log back in.

## Notes

- **Ubuntu:** several packages (bspwm, polybar...) come from the *universe* repository. It is enabled by default, but if `apt` can't find them, enable it with `sudo add-apt-repository universe`.
- **Firefox (`--all` mode):** Debian, Kali and Parrot get `firefox-esr`. Ubuntu-based distros already include Firefox, so bspwmctl doesn't install it there.
- **Linux Mint, Pop!_OS and other derivatives** are not tested yet. They should work, and bspwmctl will warn you about it. Please [report](https://github.com/bspwmctl/bspwmctl/issues) any problem.
