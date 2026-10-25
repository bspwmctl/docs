# Contributing

Thank you for your interest in contributing! 🎉

## Ways to contribute

- 🐛 **Report a bug:** [open a bug report](https://github.com/bspwmctl/bspwmctl/issues/new?labels=bug&template=bug_report.md). Include your distro, the bspwmctl version (`bspwmctl --version`) and the full output.
- 💡 **Suggest a feature:** [open a feature request](https://github.com/bspwmctl/bspwmctl/issues/new?labels=enhancement&template=feature_request.md).
- 🧪 **Test on your distro:** especially derivatives that aren't tested yet (Linux Mint, Pop!_OS, Manjaro, Garuda, Nobara...). Reporting that it works is useful too.
- 📖 **Improve the docs:** fix typos, unclear steps or add screenshots in the [docs repository](https://github.com/bspwmctl/docs).
- 🎨 **Share themes and scripts:** the [themes](https://github.com/bspwmctl/themes) and [scripts](https://github.com/bspwmctl/scripts) repositories are coming soon.

## Contributing code

Read the [Contributing Guide](https://github.com/bspwmctl/bspwmctl/blob/main/.github/CONTRIBUTING.md) first. In short:

```bash
# Fork the repo on GitHub, then:
git clone https://github.com/YOUR_USERNAME/bspwmctl.git
cd bspwmctl
git checkout -b feature/your-feature-name

# ...make your changes...

git commit -m "Add: brief description of your changes"
git push origin feature/your-feature-name
```

Then open a pull request against `main`.

### Before opening a pull request

```bash
bash -n bspwmctl                                  # syntax check
shellcheck --severity=warning bspwmctl            # lint
./packaging/build.sh                              # build the packages (needs Docker or nfpm)
```

- `bspwmctl install` really installs packages and replaces your configs, so **test it in a VM or a container**, not on your daily machine.
- If you add a package, check that it exists with that name in Debian/Ubuntu, Arch and Fedora (names often differ).
- Every pull request runs the same checks on GitHub Actions, and installs the packages on Ubuntu, Debian, Fedora and Arch.

### Code style

- Bash with `set -Eeuo pipefail`, 2-space indentation
- Use the `log`, `success`, `warn` and `die` helpers for output
- Bundled configs must work on any machine: no hardcoded monitors, network interfaces or home paths

## Getting help

Not sure about something? [Open a question](https://github.com/bspwmctl/bspwmctl/issues/new?labels=question&template=question.md) or ask in your pull request.
