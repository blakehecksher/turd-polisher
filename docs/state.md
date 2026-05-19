# State
_Last updated: 2026-05-18 2053_

## Current focus
Mobile-friendly pass complete for the playable single-file `index.html`.

## What's working
- Title -> intro card -> camera-zoom turd drop with splash -> polish phase -> result screen -> next round
- Procedural turd geometry, toilet, animated water plane, custom turd shader, and RGBA8 polish texture painting
- Raycast painting from pointer drag with brush/cloth/wax/spray tools
- Desktop keyboard controls: 1-4 tool switching and WASD rotation
- Mobile/touch controls: tap tools, drag to polish, on-screen rotate pad, touch-safe viewport behavior, and iPhone safe-area spacing
- Procedurally synthesized SFX, difficulty escalation, modifiers, HUD gauges, timer, grade result, and confetti

## In progress
Nothing. Mobile-friendly pass is complete.

## Known issues
- Headless emoji glyphs render as boxes in some browsers (cosmetic; real users get OS emoji).
- Outline material isn't disposed when turd respawns (tiny leak per round; negligible).
- Reaching S grade in 15s is hard - by design, but may want tuning after playtest.
- Browser plugin Node bridge was unavailable in this session, so verification was limited to static source inspection and module syntax checking.

## Next actions
1. Playtest on a real iPhone Safari/Chrome session and tune control placement if needed.
2. Playtest several rounds; tune tool strengths/radii if S-grade is too hard or too easy.
3. Add more turd archetypes (nugget cluster, twisty rope).
4. Optional: persistent high-score in localStorage.

## Active plan
docs/plans/2026-05-18 2032 Plan - Mobile Friendly.md  (status: complete)

## Recent logs
- docs/log/2026-05-18 2053 Git Ignore.md - replaced the blunt PNG ignore with repo-specific rules and untracked generated local artifacts.
- docs/log/2026-05-18 2032 Mobile Friendly.md - added iPhone/touch layout, pointer handling, and rotate controls.
- docs/log/2026-05-17 2322 Kickoff.md - project initialized, spec + plan written.
- docs/log/2026-05-17 2338 v1 Build.md - single-pass build of `index.html`; smoke-tested end-to-end via Playwright.
