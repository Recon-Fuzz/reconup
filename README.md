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

Since Recon Fuzzer is in a private repository, you need a GitHub personal access token with `repo` scope.

### Option 1: Pass token as argument

```bash
reconup <your_github_token>
```

### Option 2: Set environment variable

```bash
export RECON_GITHUB_TOKEN=<your_token>
reconup
```

For persistence, add the export to your shell profile (`~/.zshrc`, `~/.bashrc`, etc.).

## Updating

Simply run `reconup` again. It will only download if a newer version is available:

```bash
reconup
```

## Supported Platforms

| Platform | Status |
|----------|--------|
| Linux x86_64 | Supported |
| macOS ARM64 (Apple Silicon) | Supported |
| macOS x86_64 (Intel) | Coming soon |
| Windows x86_64 | Coming soon |

## Installation Directory

By default, recon is installed to `~/.recon/bin/recon`. You can customize this by setting the `RECON_DIR` environment variable before running the installer:

```bash
export RECON_DIR=/custom/path
curl -L https://raw.githubusercontent.com/Recon-Fuzz/reconup/refs/heads/main/install | bash
```

## Uninstall

```bash
rm -rf ~/.recon
```

Then remove the PATH export from your shell profile.
