# Vibeloft

**A room for every project.** A desktop workspace for Claude Code projects, by Leadows.

Vibeloft keeps every customer project in one place: the code, a terminal running Claude Code, features and bugs, delivery dates, time tracking and status reports.

This repository holds the Vibeloft installers and release notes. The source code is kept separately.

## Download

<!-- latest:start -->
**Latest version: 0.6.0** (25 November 2026)

[Download Vibeloft-Setup-0.6.0.exe](https://github.com/Leadows-AI/vibeloft-releases/releases/download/v0.6.0/Vibeloft-Setup-0.6.0.exe) for Windows
<!-- latest:end -->

All versions are on the [Releases](https://github.com/Leadows-AI/vibeloft-releases/releases) page.

## Install on Windows

1. Download `Vibeloft-Setup-<version>.exe` from the latest release.
2. Run it. Vibeloft installs for your Windows user (no admin rights needed); you can change the folder. It adds Start menu and desktop shortcuts.
3. Windows may show **"Windows protected your PC"** because the installer isn't code-signed yet. Click **More info**, then **Run anyway**.

## What you need

- **Claude Code**, signed in. Vibeloft uses the Claude Code installed on your computer.
- **Git**.
- **GitHub CLI** (optional), for cloning repositories and syncing issues.

On first start, Vibeloft checks for these and can install any that are missing.

## Updates

Vibeloft updates itself. Every 4 hours it checks for a new version and downloads it in the background. The update installs when you close Vibeloft, or straight away if you click **Restart to update** in the sidebar. To check right now, open **Settings → Updates → Check now**.

## Your data

Everything Vibeloft stores is in one file on your computer:

- Windows: `%APPDATA%\Vibeloft\studio.json`
- macOS: `~/Library/Application Support/Vibeloft/studio.json`

Back it up by copying that file. Updating or reinstalling Vibeloft keeps it.

## Release notes

<!-- changelog -->

### 0.6.0 (25 November 2026)

- Archive or delete a project
- Fonts: choose interface and code fonts from Google Fonts
- Setup check, Claude Code hooks, and Claude jobs without the Agent SDK

<!-- last-commit: 33b2d0d -->

## About

Vibeloft is an independent project built on Claude Code. It is not an Anthropic product and is not affiliated with or endorsed by Anthropic.
