status: complete

# Plan - Mobile Friendly
_Created: 2026-05-18 2032_

## Goal
Make the existing single-file game practical to play on iPhone-sized touch screens.

## Steps
1. Add touch-safe viewport/layout CSS with safe-area padding and small-screen control sizing.
2. Improve pointer handling so touch painting starts immediately and does not trigger browser gestures.
3. Add mobile rotate controls so players can reach all sides without a keyboard.
4. Smoke-test the file and update project state/log docs.

## Notes
- Keep the game single-file and procedural.
- Prefer simple on-screen controls over changing the core polish loop.
