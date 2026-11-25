# Vibeloft

**A room for every project.** A desktop workspace for Claude Code projects, by Leadows.

Vibeloft keeps every customer project in one place: the code, a terminal running Claude Code, features and bugs, delivery dates, time tracking and status reports.

This repository holds the Vibeloft installers and release notes. The source code is kept separately.

## Download

<!-- latest:start -->
**Latest version: 0.10.0** (25 November 2026)

- Windows installer (recommended, updates itself): [Vibeloft-Setup-0.10.0.exe](https://github.com/Leadows-AI/vibeloft-releases/releases/download/v0.10.0/Vibeloft-Setup-0.10.0.exe)
- Windows portable (no install, no automatic updates): [Vibeloft-Portable-0.10.0.exe](https://github.com/Leadows-AI/vibeloft-releases/releases/download/v0.10.0/Vibeloft-Portable-0.10.0.exe)
<!-- latest:end -->

All versions are on the [Releases](https://github.com/Leadows-AI/vibeloft-releases/releases) page.

## Install on Windows

1. Download `Vibeloft-Setup-<version>.exe` from the latest release.
2. Run it. Vibeloft installs for your Windows user (no admin rights needed); you can change the folder. It adds Start menu and desktop shortcuts.
3. Windows may show **"Windows protected your PC"** because the installer isn't code-signed yet. Click **More info**, then **Run anyway**.

### Portable version

Each release also has `Vibeloft-Portable-<version>.exe`, which runs without installing: put it anywhere (a USB stick works) and double-click it. It keeps your data in the same place as the installed app. The portable version doesn't update itself; download the new one from the latest release when you want to update. Windows may show the same SmartScreen warning.

## What you need

- **Claude Code**, signed in. Vibeloft uses the Claude Code installed on your computer.
- **Git**.
- **GitHub CLI** (optional), for cloning repositories and syncing issues.

On first start, Vibeloft checks for these and can install any that are missing.

## Updates

The installed Vibeloft updates itself. Shortly after it starts and every 4 hours, it reads the `latest.yml` manifest of the newest release here, downloads the installer it names and checks it. The update installs when you close Vibeloft, or straight away if you click **Restart to update** in the sidebar.

In **Settings → About & updates**:

- **Check now** looks for a new version straight away.
- Untick **Check for and download updates automatically** to stop automatic checks. **Check now** still works. (From version 0.7.0.)

The portable version never updates itself.

## Your data

Everything Vibeloft stores is in one file on your computer:

- Windows: `%APPDATA%\Vibeloft\studio.json`
- macOS: `~/Library/Application Support/Vibeloft/studio.json`

Back it up by copying that file. Updating or reinstalling Vibeloft keeps it.

## Release notes

<!-- changelog -->

### 0.10.0 (25 November 2026)

- Clearer Claude controls in the Terminal tab
- Open the project folder from the file tree and project menu
- Collapsible sidebar and a project file tree

### 0.8.0 (25 November 2026)

- Keep Claude Code's important notices on screen in the Terminal tab

### 0.7.0 (25 November 2026)

- Updates from the release manifest, automatic updates switch, portable in releases

### 0.6.0 (25 November 2026)

- Archive or delete a project
- Fonts: choose interface and code fonts from Google Fonts
- Setup check, Claude Code hooks, and Claude jobs without the Agent SDK

<!-- last-commit: 07b06f3 -->

## About

Vibeloft is an independent project built on Claude Code. It is not an Anthropic product and is not affiliated with or endorsed by Anthropic.
