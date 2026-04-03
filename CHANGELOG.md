# Changelog

All notable changes to Scaffold are documented here.

---

## [1.0.1] — 2026-04-02

### New
- **Premiere Pro — Named bins with label colors**: Replace the single "Create bins" checkbox with a dynamic list. Default bins (Footage, Audio, GFX, Sequences, Exports) are pre-populated with editable names and color swatches. Add or remove bins freely. Colors are mapped to the nearest Premiere label index in the generated ExtendScript.
- **Premiere Pro — ExtendScript help button**: A `?` icon next to the ExtendScript section header explains how to run `scaffold_premiere_setup.jsx` from within Premiere Pro.

---

## [1.0.0] — 2026-04-02

### Initial Release

- **Basic tab**: Set Projects Destination, Starters Folder, and Folder Structure template. Project name with optional date prefix. One-click project creation.
- **After Effects**: Starter `.aep` copied and renamed. Comp duration, FPS, render output, and Project Panel folder creation configured. Auto-applies on first open via `scaffold_ae_watcher.jsx` (installed to AE Startup folder).
- **Cinema 4D**: Starter `.c4d` copied and renamed. Render engine, frame step, linear workflow, texture paths, and multi-pass configured. Auto-applies on first open via `scaffold_autosetup.pyp` (installed to C4D user plugins folder).
- **Premiere Pro**: Starter `.prproj` copied and renamed. ExtendScript sidecar (`scaffold_premiere_setup.jsx`) generated for bins, media cache, sequence creation, and auto-save.
- **DaVinci Resolve**: Starter `.drp` copied and renamed. Python sidecar (`scaffold_resolve_setup.py`) generated for resolution, FPS, color science, timeline settings, and proxy/cache paths.
- **Flame**: Automatic project creation via Wiretap. MediaHub bookmarks written. Archive script generated per workstation.
- **Illustrator / InDesign / Photoshop**: Starter files copied and renamed.
- **Preferences**: Per-user, per-machine settings stored in `~/.scaffold_prefs.json`. Licence key stored in macOS Keychain.
- **First-launch onboarding**: Auto-configures prefs when siblings are found; asks only for Projects Destination.
- **Uninstaller**: Double-clickable `Uninstall Scaffold.command` removes app, prefs, and Keychain entry.
