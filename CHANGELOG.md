<!-- last-commit-count: 50 -->
# TOSAYN Changelog

## 0.2.260711.50 — 2026-07-11

- Fix Sparkle update detection: build number must outrank the legacy 710 placeholder

## 0.2.260711.49 — 2026-07-11

- (no code changes since the last release)

## 0.2.260711.49 — 2026-07-11

- Add What's New menu link, wire changelog auto-generation into release.sh
- Auto-versioning: 0.2.<date>.<commit count>, computed at release time
- Feedback email includes system + scanner diagnostics
- Feedback button — mailto, no backend
- Buyer README zipped next to the app
- macOS 15 deployment target (optimizer-crash workaround) — republished
- Deployment target macOS 14 — the app no longer demands this year's macOS
- Self-contained releases: engine embedded in the bundle, one-shot release script
- Sparkle 2 auto-updates with EdDSA-signed appcast
- App icon actually shows up: partial Info.plist with the icon keys, versions unmangled
- Traffic lights, About panel with NAPS2 attribution, update check, version 0.1.710
- Lighthouse app icon and in-app logo (leuchtturm.svg)
- Tooltip previews the hovered tab's settings
- Settings tooltip: hover-driven, auto-fading, floating, fit to content
- Preset chevron only on the active tab
- Preset dropdown: hover trash to delete; short names center in the tab
- 'Save as preset…' is always visible — the drawer height never changes again
- Preset tab: constant width, sized like the word 'Preset'
- Preset tab: plain truncated name instead of the marquee
- Kill the tab-switch party: single always-present pill, scoped animations, height stability
- Tab bar rebuilt as one uniform construction: no more Doc… truncation, no pill jump
- Tabs hug their text, chevron stays visible right of a marquee name, and tab switches no longer make the settings text jump
- Preset tab: real tab + chevron-only custom picker
- Preset tab shows its active state
- Main window rebuilt as the settings-panel construction: borderless NSWindow + NSHostingView, no sizing code at all
- Main window sized by SwiftUI like the settings panel; preset tab is the dropdown; status line removed
- Presets store OCR, batch, and optionally the save-to folder
- Settings back in a separate window — main window never resizes
- Drawer slides via window edge only; layout + settings-weight fixes
- Settings polish: flat white drawer, smaller toggles, tighter rhythm
- Interface cleanup: gallery in its own resizable window, quieter settings
- V2: one window — gallery and settings slide out via animated window frame
- Design P0/P1: settings regrouped, calibration retired, chips + success moment
- Browser toolbar: labeled icons, grouped by intent (DESIGN.md P0-3)
- Add design review & redesign plan (DESIGN.md)
- Store raw scanner data: lossless PNG archive per scan, edits work from raw
- Fix linear-vs-sRGB levels mismatch; Auto handles underexposed scans
- Levels slider v3: glass knobs, nearest-nub gesture, full-height histogram
- Engine: trim near-black scanner borders per page
- Magic Auto: edge-based ink/paper detection, validated on real receipts
- Levels slider: fix undraggable black nub, flat native knobs, live histogram
- Preview zoom: drop autoScales entirely, fit manually until the user zooms
- Fix slider nubs dragging the window and preview zoom snapping back
- Magic editor: real levels sliders + histogram, sticky selection preview, viewport handover
- Fix black pages from magic adjust: sampling read vertically mirrored pixels
- Magic editor: zoom + pan, pixel loupe, auto-set, step-back and file undo
- Fully-auto scanning: per-page auto-levels, Vision OCR, crop/magic page editor
- TOSAYN: SwiftUI scanner app + NAPS2.Sdk engine build script
