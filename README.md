# macOS Installer Downloader

[![Build macOS Installer ISO/DMG image](https://github.com/yhpgi/macos_downloader/actions/workflows/build.yaml/badge.svg)](https://github.com/yhpgi/macos_downloader/actions/workflows/build.yaml)

This repository provides a fully automated GitHub Actions workflow to download official macOS installers directly from Apple's servers and convert them into bootable ISO or DMG images.

The generated images are uploaded as workflow artifacts, making them accessible for virtual machines, system recovery, or other development needs.

## Features

-   **Fully Automated:** Uses GitHub Actions for a serverless, "no-setup" experience.
-   **Official Sources:** Downloads installers directly and securely from Apple's software update servers.
-   **Multiple Formats:** Creates both `.iso` (for virtual machines) and `.dmg` (for USB installers) files.
-   **Wide OS Support:** Capable of building installers for a range of macOS versions, from High Sierra to the latest release.
-   **Workflow Artifacts:** Uploads the final image(s) as artifacts to the specific workflow run that generated them.
-   **Efficient Caching:** Caches the downloaded installer to significantly speed up subsequent builds of the same version, saving time and runner costs.

## How to Use

To use this workflow for your own builds, please follow these steps:

1.  **Fork this Repository:** Click the "Fork" button at the top-right of this page to create a copy of this repository under your own GitHub account.

2.  **Navigate to the Actions Tab:** In your forked repository, go to the **Actions** tab. You may need to enable GitHub Actions if prompted.

3.  **Run the Workflow:**
    -   In the left sidebar, click on the **"Build macOS Installer ISO/DMG image"** workflow.
    -   Click the **"Run workflow"** dropdown button on the right side.

4.  **Configure the Build:**
    -   **Select a macOS version to build:** Choose the desired OS from the dropdown (e.g., `Sonoma`, `Ventura`).
    -   **Select image format(s) to build:** Choose `iso`, `dmg`, or `both`.
    -   Click the green **"Run workflow"** button to start the build.

5.  **Download the Artifact:**
    -   The workflow will take approximately 20-60 minutes to complete, depending on the format and whether the installer is cached.
    -   Once the workflow is complete, navigate to the summary page for that specific run. The generated images will be available for download in the **"Artifacts"** section at the bottom of the page.
    -   **Note:** Workflow artifacts are temporary and will expire after a set period (configured for 7 days by default).

## Disclaimer

-   **Software Licensing:** This tool only automates the download of official software provided by Apple. You are responsible for adhering to Apple's End User License Agreement (EULA) for macOS.
-   **Intended Use:** This project is intended for legitimate purposes, such as creating installers for virtual machines for software development, or for creating bootable USB drives to reinstall macOS on genuine Apple hardware.
-   **Non-Apple Hardware ("Hackintosh"):**
    -   To install macOS on non-Apple hardware, a specialized bootloader such as **OpenCore** is required. The `.dmg` file produced by this workflow contains the installer, but it will not boot on a PC without a correctly configured OpenCore EFI.
    -   For building a "Hackintosh", we strongly recommend following the official **[Dortania's OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/)**.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
