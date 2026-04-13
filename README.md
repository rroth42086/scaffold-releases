# Scaffold

**One-click project setup for video and motion editors.**

Scaffold is a macOS utility that creates a standardized folder structure for every new project — copying starter files, generating per-app setup scripts, and optionally creating a Flame project via Wiretap. Open your app, open your project, and everything is already in place.

Built for After Effects · Cinema 4D · Flame · DaVinci Resolve · Premiere Pro · Illustrator · InDesign · Photoshop

---

## Download

[**Download the latest release →**](https://github.com/rroth42086/scaffold-releases/releases/latest)

Requires macOS 12 or later · Apple Silicon native · Runs on Intel via Rosetta 2

---

## Install

1. Open `Scaffold.dmg`
2. Drag **Scaffold** into Applications
3. Right-click `Scaffold.app` → **Open** on first launch (required until the app is notarized)

The `scaffold_structure/`, `scaffold_starters/`, and `Uninstall Scaffold.command` files inside the DMG must remain in the same folder as `Scaffold.app` — the drag installs them together automatically.

---

## First Launch

Scaffold walks you through a one-time setup:

- **Projects Destination** — the root folder where new projects are created (e.g. `/Volumes/WORK/Projects`)
- **Starters Folder** — the folder containing your starter files (`_template.aep`, `_template.c4d`, etc.)
- **Folder Structure** — the template directory whose layout is copied into every new project

These are saved to `~/.scaffold_prefs.json` and can be changed any time via **Preferences**.

---

## What Happens When You Create a Project

1. A new folder is created at `<Projects Destination>/<ProjectName>`
2. The full folder structure from your template is recreated inside it
3. Starter files are copied from your Starters Folder into the appropriate app subfolders and renamed to match the project
4. Per-app setup scripts are generated next to each project file
5. If Flame is enabled and the Wiretap daemon is running, a Flame project is created automatically and MediaHub bookmarks are written

---

## Per-App Features

### After Effects
- Starter `.aep` copied and renamed
- Comp duration and FPS configured in the template
- Render output path set as a preference
- Project panel folders created on first open (auto-applies via a watcher script installed to AE's Startup folder)

### Cinema 4D
- Starter `.c4d` copied and renamed
- Render engine, frame step, linear workflow, texture paths, and multi-pass configured via an auto-plugin installed to C4D's user plugins folder

### Premiere Pro
- Starter `.prproj` copied and renamed
- **ExtendScript sidecar** (`scaffold_premiere_setup.jsx`) generated in the project's Premiere folder
- Run once from Premiere via **File > Scripts > Run Script File...** to apply:
  - Named Project Panel bins with label colors
  - Media cache path
  - Starter sequence
  - Auto-save interval

### DaVinci Resolve
- Starter `.drp` copied and renamed
- **Python sidecar** (`scaffold_resolve_setup.py`) generated in the project's DaVinci folder
- Run once from Resolve via **Workspace > Console** to apply:
  - Resolution and frame rate
  - Color science mode
  - Timeline settings
  - Proxy and cache paths

### Flame
- Project created automatically via Wiretap (`127.0.0.1:IFFFS`) — no manual steps
- MediaHub bookmarks written to `setups/status/cf_bookmarks.json`
- Archive script generated per workstation

### Illustrator / InDesign / Photoshop
- Starter file copied and renamed into the project folder

---

## Uninstall

Double-click `Uninstall Scaffold.command` (included in the DMG and in `/Applications/Scaffold/`).

This removes:
- `/Applications/Scaffold/`
- `~/.scaffold_prefs.json`
- The licence key from your macOS Keychain

---

## Support

Use the **Feedback** button inside the app (menu bar → **Help > Send Feedback**) to report bugs or request features.

---

© 2026 Route 86 Visuals LLC. All Rights Reserved.
