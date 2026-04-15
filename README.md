# reconup

Installer and updater for [Recon Fuzzer](https://github.com/Recon-Fuzz/recon-fuzzer).

## Installation

```bash
curl -L https://raw.githubusercontent.com/Recon-Fuzz/reconup/refs/heads/main/install | bash
```

Then restart your shell or run:

```bash
source ~/.zshrc  # or ~/.bashrc
```

## Usage

Install the latest `recon` release:

```bash
reconup
```

## Updating

Run `reconup` again. It only downloads if a newer release is available.

## Supported Platforms

| Platform | Status |
|----------|--------|
| Linux x86_64 | Supported |
| macOS ARM64 (Apple Silicon) | Supported |
| macOS x86_64 (Intel) | Coming soon |
| Windows x86_64 | Coming soon |

## Installation Directory

By default, `recon` is installed to `~/.recon/bin/recon`. Override with the `RECON_DIR` environment variable before running the installer:

```bash
export RECON_DIR=/custom/path
curl -L https://raw.githubusercontent.com/Recon-Fuzz/reconup/refs/heads/main/install | bash
```

## Uninstall

```bash
rm -rf ~/.recon
```

Then remove the PATH export from your shell profile.
