# Decisions

Append-only. One entry per decision. Before adding, scan for conflicts with existing entries.

---

<!-- entries go below this line -->

## 2026-05-17 2322 — Single-file HTML + Three.js ESM via unpkg

Decision: Ship as one self-contained `index.html` using `import * as THREE from 'https://unpkg.com/three@0.160.0/build/three.module.js'`.
Reason: User wanted a complete, runnable artifact with zero setup. ESM import works directly in modern browsers and skips bundler/build tooling.

## 2026-05-17 2322 — All assets procedural

Decision: No external image, model, or audio files. Geometry, textures, and SFX all generated at runtime.
Reason: Keeps the project a single-file artifact; avoids asset-licensing concerns; reinforces the cartoon/toy feel.

## 2026-05-17 2322 — Polish state as a single RGBA8 DataTexture

Decision: Pack the four polish channels (filth / roughness / gloss / sparkle) into one 256×128 RGBA UnsignedByte DataTexture; paint from CPU on raycast hits.
Reason: Resolution is small enough that CPU writes are cheap, channel packing keeps the shader simple (one texture sample), and avoids the boilerplate of a render-to-texture pipeline. Acceptable visual granularity for a 15-second polish round.
