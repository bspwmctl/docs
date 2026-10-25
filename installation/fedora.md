# Fedora

This guide covers Fedora and its derivatives (Nobara...).

## 1. Install bspwmctl

Download the `.rpm` from the [latest release](https://github.com/bspwmctl/bspwmctl/releases) and install it:

```bash
sudo dnf install ./bspwmctl-*.noarch.rpm
```

## 2. Install the desktop

As your normal user:

```bash
bspwmctl install --standard
```

## 3. Log in to bspwm

Log out, choose **bspwm** in the session menu of your login screen and log back in. If it isn't listed, see [bspwm doesn't appear in the login screen](installation/?id=bspwm-doesnt-appear-in-the-login-screen).

## Notes

- **RHEL, CentOS, Rocky and AlmaLinux are not supported:** bspwm and most of the desktop are not in their repositories.
- **Nobara and other derivatives** are not tested yet. They should work, and bspwmctl will warn you about it. Please [report](https://github.com/bspwmctl/bspwmctl/issues) any problem.
