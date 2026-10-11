# macOS Installer Downloader

[![Build macOS Installer ISO/DMG image](https://github.com/yhpgi/macos_downloader/actions/workflows/build.yaml/badge.svg)](https://github.com/yhpgi/macos_downloader/actions/workflows/build.yaml)

Download official macOS installers from Apple and build ISO or DMG images using GitHub Actions. No local setup required.

## Features

- **Official downloads** — Retrieves installers directly from Apple's servers.
- **Multiple formats** — Build `.iso`, `.dmg`, or both.
- **Multiple macOS versions** — From High Sierra to supported newer releases.
- **Caching** — Reuses cached installers to reduce build time.
- **Artifacts** — Download generated images directly from GitHub Actions.

## Usage

1. **Fork** this repository.
2. Open the **Actions** tab in your fork.
3. Select **Build macOS Installer ISO/DMG image**.
4. Click **Run workflow**.
5. Choose the macOS version and image format (`iso`, `dmg`, or `both`).
6. Start the workflow and wait for it to complete.
7. Download the generated image from the run's **Artifacts** section.

Builds typically take 20–60 minutes, depending on the selected format and cache availability. Artifacts expire after 7 days by default.

## Compatibility Notes

- **Virtual machines:** Use the generated ISO with a compatible VM.
- **Apple hardware:** Use the appropriate image for your installation or recovery workflow.
- **Non-Apple hardware:** A DMG alone is not sufficient to boot macOS on a PC. A compatible bootloader and configuration are required. See the [Dortania OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/).

## Disclaimer

You are responsible for complying with Apple's macOS Software License Agreement and applicable terms of use.

## License

[MIT](LICENSE)
