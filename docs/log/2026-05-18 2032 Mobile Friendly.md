# 2026-05-18 2032 - Mobile Friendly

## What was done
- Added touch-safe viewport CSS, safe-area spacing, and small-screen HUD/tool tray sizing.
- Added a mobile-only rotate pad so the turd can be rotated without WASD.
- Reworked pointer handling so touch painting starts on pointer-down, uses canvas-relative raycast coordinates, prevents iOS browser gestures during play, and handles pointer cancellation.
- Updated renderer/camera sizing to account for `visualViewport` changes.

## What worked
- Existing single-file structure was preserved.
- Node module syntax check passed after stripping the CDN import for local syntax validation.

## What didn't and why
- The Browser plugin Node bridge was not exposed in this session, so an in-app browser/iPhone viewport visual check could not be performed.

## Decisions made
none

## Left unfinished
- Real-device iPhone playtest and any follow-up tuning from that playtest.

## state.md updated: yes
