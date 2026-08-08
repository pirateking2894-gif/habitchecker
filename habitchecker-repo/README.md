# HabitChecker

A simple SwiftUI habit-tracking app, built into an unsigned `.ipa` via
GitHub Actions (no Mac, no Apple Developer account needed) for use with
LiveContainer.

## How the build works

- `project.yml` — describes the iOS app target. `xcodegen` (installed
  automatically by the workflow) turns this into a real `.xcodeproj` —
  you never need to open Xcode yourself.
- `Sources/HabitChecker.swift` — the entire app.
- `.github/workflows/build-ipa.yml` — runs on GitHub's free macOS
  runners, builds the app unsigned, zips it into `HabitChecker.ipa`,
  and uploads it as a downloadable artifact.

## Building

Push to `main`, or go to the **Actions** tab → **Build IPA** →
**Run workflow**. When it finishes, open the run and download the
`HabitChecker-ipa` artifact — it contains `HabitChecker.ipa`.

## Installing

Transfer `HabitChecker.ipa` to your iPhone (AirDrop, iCloud Drive,
Files app, email to yourself, etc.) and import it into LiveContainer.
