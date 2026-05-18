# State
_Last updated: 2026-05-17 2338_

## Current focus
v1 build complete. Playable single-file `index.html`.

## What's working
- Title → intro card → camera-zoom turd drop with splash → 15s polish phase → result screen → next round
- Procedural turd geometry (parametric coil + value-noise displacement; archetypes: coil, spiral, blob, logger)
- Procedural toilet (lathe profile), animated water plane with caustic shader + splash ripple
- Custom turd shader: per-channel painting (filth / roughness / gloss / sparkle) via RGBA8 DataTexture, bump from roughness, specular from gloss, sparkle dots, corn + glitter modifiers
- Raycast painting from mouse drag, weighted radial brush, wraps V-axis
- 4 tools: brush/cloth/wax/spray with distinct radius/strength/SFX/particles, hotkeys 1–4
- Cartoon outline (back-side dilated mesh), screen shake on plop, HUD gauges + animated timer bar, big grade letter pop, confetti
- Procedurally-synthesized SFX (no audio assets): plop, splash, scrub, wipe, wax, spray, zoom, countdown, fanfare per-grade, buzz
- Difficulty escalation: shorter timer (16→8s), more aggressive archetypes from round 3, corn/glitter modifiers from round 2+
- Difficulty modifiers: corn flecks, baseline glitter, veryDirty rounds

## In progress
Nothing. Closing session.

## Known issues
- Headless emoji glyphs render as boxes in some browsers (cosmetic; real users get OS emoji).
- Outline material isn't disposed when turd respawns (tiny leak per round; negligible).
- No touch/mobile-optimized hit area on tool tray buttons (keys 1–4 work; click works).
- Reaching S grade in 15s is hard — by design, but may want tuning after playtest.

## Next actions
1. Playtest several rounds; tune tool strengths/radii if S-grade too hard or too easy.
2. Add more turd archetypes (nugget cluster, twisty rope).
3. Add per-round modifier callouts ("CORN ROUND!").
4. Optional: persistent high-score in localStorage.

## Active plan
docs/plans/2026-05-17 2322 Plan - v1 Build.md  (status: complete)

## Recent logs
- docs/log/2026-05-17 2322 Kickoff.md — project initialized, spec + plan written.
- docs/log/2026-05-17 2338 v1 Build.md — single-pass build of `index.html`; smoke-tested end-to-end via Playwright.
