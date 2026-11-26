# Vibeloft

**A room for every project.** A desktop workspace for Claude Code projects, by Leadows.

Vibeloft keeps every customer project in one place: the code, a terminal running Claude Code, features and bugs, delivery dates, time tracking and status reports.

This repository holds the Vibeloft installers and release notes. The source code is kept separately.

## Download

<!-- latest:start -->
**Latest version: 0.18.0** (26 November 2026)

- Windows installer (recommended, updates itself): [Vibeloft-Setup-0.18.0.exe](https://github.com/Leadows-AI/vibeloft-releases/releases/download/v0.18.0/Vibeloft-Setup-0.18.0.exe)
- Windows portable (no install, no automatic updates): [Vibeloft-Portable-0.18.0.exe](https://github.com/Leadows-AI/vibeloft-releases/releases/download/v0.18.0/Vibeloft-Portable-0.18.0.exe)
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

### 0.18.0 (26 November 2026)

- Settings: Claude, Git and Updates get their own tabs; updater treats a release without latest.json as up to date; npm run release now builds and publishes the Rust app (latest.json + latest.yml so Electron copies move over); installer restarts Vibeloft after Electron's silent update
- Vibeloft 0.17.0 on Rust: real Vibeloft identity and data folder, installer removes the Electron app (data kept, studio.json backed up), updater reads the newest release
- Settings → About: 'Powered by' with the technologies and their logos (Tauri/Rust or Electron/Node.js by build)
- Field test: Tauri updater (signed, rust-latest manifest), Rust 0.15.0, opt-in 'Try the new Vibeloft' card in Electron, NOTES option for releases
- Wire the Rust modules together: shared data folder (seeded from Electron's data and usage), close guard counts terminals, one Claude lookup, gitops' staged diff and git for commit messages and links, JSON key order kept
- Merge branch 'worktree-agent-aa9d6be272a217dda' into rust-tauri
- Merge branch 'worktree-agent-abbb524547431bcaf' into rust-tauri
- Ignore agent worktrees
- Merge branch 'worktree-agent-a82dfba4ddf26db85' into rust-tauri
- Rust port: git, Git tab, checkpoints and GitHub (folder:*, git:*, checkpoint:*, gh:*)
- Rust backend groundwork: one module per TS main file with handle(), shared util (args, run, emit), stubs for cross-module calls
- Rust build starts at 0.14.0, the Electron version it branched from
- release:rust: publish to vibeloft-releases as rust-v* pre-releases that never become latest
- Rust build: theme follows settings, own data folder, version 0.1.0, release:rust to a separate releases repo
- Tauri + Rust spike: same React UI on a Rust backend (data, files, terminals), separate Vibeloft Rust identity

### 0.16.0 (26 November 2026)

- Try the new Vibeloft (field test): Settings → This computer has a card to download Vibeloft rebuilt on Rust. It installs next to this app with a copy of your projects, so nothing here changes and you can switch back any time.

### 0.15.0 (26 November 2026)

- Claude tokens and cost per project
- Add graphify knowledge graph (graph.json, graph.html, GRAPH_REPORT.md)

### 0.14.0 (26 November 2026)

- Material file icons, tighter layout, header help, Settings tiles and tabs, About Leadows

### 0.13.0 (26 November 2026)

- Streamlined project window: one-row header with More tab menu, single + menu in the terminal toolbar, git/Claude footer

### 0.12.0 (25 November 2026)

- Mobile tab for mobile app projects: build an APK ("for this phone" builds several times faster), install it on a connected phone, device logs, and Fix with Claude / Send crash to Claude
- Claude Code ending in a tab, Ctrl+C, and Claude carrying on by itself are now handled properly

### 0.11.0 (25 November 2026)

- Several git repositories in one project folder

### 0.10.1 (25 November 2026)

- Fix Claude conversations not saved or quitting at start

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

<!-- last-commit: 420dd8b -->

## About

Vibeloft is an independent project built on Claude Code. It is not an Anthropic product and is not affiliated with or endorsed by Anthropic.
