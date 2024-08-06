# DriverGuard

🚀 **DriverGuard** - The ultimate tool to swiftly scan your computer for known vulnerable and malicious Windows drivers using the power of LOLDrivers.io!

## Overview:

DriverGuard is designed to protect your system by detecting and flagging potentially dangerous drivers. Leverage the extensive LOLDrivers database to keep your computer secure with lightning-fast scans and detailed reports.

## Getting Started:

### Quick Start

To start using DriverGuard, simply download the prebuilt binaries or build it from source. Choose your preferred operating mode and scan options to tailor the tool to your needs.

### Installation:

#### Prebuilt Binaries

Grab the latest prebuilt binaries from the [Releases](https://github.com/rtfmkiesel/loldrivers-client/releases) page and get started instantly.

#### Building from Source:

```sh
git clone https://github.com/rtfmkiesel/loldrivers-client
cd loldrivers-client
go mod tidy
go build -o DriverGuard.exe -ldflags="-s -w" cmd/loldrivers-client/loldrivers-client.go
```
Usage:
```
DriverGuard.exe [flags]

Flags:
Operating Modes:
  -m, --mode string        Select mode: {online, local, internal} (default "online")
  -f, --driver-file string Specify path to 'drivers.json' for local mode

Scan Options:
  -d, --scan-dir string  Directory to scan (default: Windows driver folders)
  -l, --scan-size int    Maximum file size to scan in MB (default 10)
  -w, --workers int      Number of checksum threads (default 20)
  -s, --suppress-errors  Hide file read errors during checksum calculation

Output Options:
  -g, --grepable  Output only found files for easy parsing
  -j, --json      Format output as JSON
```

Key Features: </br>
Multiple Operating Modes: Choose between online, local, and internal modes to fit your environment.
Customizable Scanning: Define directories, file size limits, and the number of checksum threads for optimized performance.
Flexible Output: Generate outputs in grepable or JSON formats for easy integration with other tools.

Contribution: </br>
DriverGuard is open to enhancements and contributions. If you're passionate about Golang and security, feel free to fork the repo and submit PRs.


