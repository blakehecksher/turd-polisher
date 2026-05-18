# Spec — Turd Polisher v1
_Created: 2026-05-17 2322_

## Concept
3D browser game. WarioWare-pace turd polishing. Turd plops into toilet, camera zooms, player picks tools, polishes against timer, gets graded. Round repeats with escalating difficulty.

## Pillars
- **Toy first**: dragging tools on turd must feel satisfying alone, before scoring.
- **WarioWare cadence**: <20s rounds, hard cuts, expressive result screens, immediate next round.
- **No assets**: 100% procedural — geometry, textures, audio. Single HTML file, no installs.

## Platform
- Single `index.html`, runs from `file://` or any static server.
- Three.js via CDN (r160).
- WebAudio for SFX (synthesized).
- Targets desktop Chrome/Firefox/Edge. Mouse only v1.

## Game loop
1. Title (PRESS TO POLISH)
2. Round intro card: "POLISH IT!" 0.8s
3. Drop: turd falls into toilet, splash, camera zooms (1.2s)
4. Polish phase: 15s timer, player drags tools across turd
5. Result: stats fly in, letter grade (F→S), particles
6. Next round with twist: weirder shape, less time, or "dirty" turd

## Polish mechanics
Four tools, each fills its own gauge by painting a data-texture on the turd:
- **Brush** — scrubs off "filth" specks
- **Cloth** — smooths bumps (reduces normal-map intensity locally)
- **Wax** — adds gloss (specular highlight)
- **Sparkle Spray** — emits particles + raises sparkle stat

Score = weighted average of four gauges × time bonus.

Grade thresholds: S 95+, A 85, B 70, C 55, D 40, F below.

## Visual style
- Cartoon: chunky outlines, saturated colors, bright key + cool rim light.
- Turd = classic coiled cone (three stacked tori narrowing up), procedurally noised.
- Toilet = simple bowl (lathed profile) + water plane with caustics shader.
- Result screen: black bars, big chunky type, confetti.

## Stretch (if cheap)
- Multiple turd archetypes (logger, spiral, nugget cluster)
- Random "modifier" each round: corn, glitter pre-applied, extra-slimy
- Combo multiplier when alternating tools

## Out of scope v1
- Mobile touch (will add if trivial)
- Persistence / high scores
- Music (SFX only)
