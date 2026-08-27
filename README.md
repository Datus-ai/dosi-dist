# dosi-dist

Download host for **Dosi** — the native engine for OSI (Open Semantic
Interchange). This repository publishes **compiled release binaries only**. It
contains no source code, and it is not where Dosi is developed.

Dosi is licensed under the [Elastic License 2.0](LICENSE) (ELv2): free to
download, use, and redistribute, in production and commercially. You may not
offer it to third parties as a hosted or managed service, circumvent its
license key functionality, or remove its licensing notices.

## Install

```console
$ curl -fsSL https://dosi.datus.ai/install.sh | sh
```

On Windows (PowerShell):

```powershell
> irm https://dosi.datus.ai/install.ps1 | iex
```

The installer picks the archive matching your OS and CPU, verifies its SHA-256,
and puts `dosi` and `dosi-server` on your `PATH`.

## Manual download

Each [release](../../releases) attaches one archive per platform, plus
`SHA256SUMS` and a `manifest.json` listing every archive with its checksum.

| Platform | Archive |
|---|---|
| Linux x86_64 | `dosi-<version>-x86_64-unknown-linux-gnu.tar.gz` |
| Linux arm64 | `dosi-<version>-aarch64-unknown-linux-gnu.tar.gz` |
| macOS Intel | `dosi-<version>-x86_64-apple-darwin.tar.gz` |
| macOS Apple Silicon | `dosi-<version>-aarch64-apple-darwin.tar.gz` |
| Windows x86_64 | `dosi-<version>-x86_64-pc-windows-msvc.zip` |

Always verify before running:

```console
$ shasum -a 256 --ignore-missing -c SHA256SUMS
```

`manifest.json` for the current release is always at:

```
https://github.com/Datus-ai/dosi-dist/releases/latest/download/manifest.json
```

## Documentation

Everything else — the CLI reference, connectors, the semantics contract, the
REST and MCP APIs — lives at **https://dosi.datus.ai/**
（[简体中文](https://dosi.datus.ai/zh/)）.

## Issues

This repository does not track Dosi issues. For support, a hosting arrangement,
or any use ELv2 does not allow, contact the Datus team.
