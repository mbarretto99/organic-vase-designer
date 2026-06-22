# OrganicVase Designer

A parametric 3D design tool for generating **organic, wave-modulated vase forms** and exporting them as **STL / 3MF files for 3D printing**.

Design organic, ruffled, twisted vase forms in minutes with sliders — forms that would take hours to model by hand in Fusion 360 or Plasticity — then export print-ready files.

![OrganicVase Designer](https://img.shields.io/badge/Three.js-0.165-62E9FB) ![No build step](https://img.shields.io/badge/build-none-success)

## Features

- **Real-time 3D viewport** (Three.js + OrbitControls) — orbit, zoom, pan, floor grid, cross-section view
- **Three-zone blend engine** (Bottom / Middle / Top) with quadratic Bernstein blending, twist + twist acceleration per zone
- **Cross-section profiles:** organic SVG star, custom wave (ripple / amplitude / sharpness / organicness), polygon (with corner rounding), ellipse, and user-imported SVG
- **Wave modulation overlay** with top/bottom zones and link toggle
- **Top adjustment** — tilt / dome / bowl with linear or curved profile
- **Wall-thickness guidance** — recommended print band + live geometry warning
- **Export** — STL (Binary / ASCII) and 3MF, at Coarse / Medium / Fine resolution
- **Save / Load** designs as `.vasedesign` JSON, with undo/redo (50 states)

## Run

It's a single self-contained HTML file — no build step, no server required.

- **Locally:** just open `index.html` in a modern browser (Chrome, Firefox, Safari, Edge).
- **Online:** visit the hosted version on GitHub Pages (enable in your repo settings → Pages → serve from root).

Three.js is loaded from a CDN (`unpkg.com`), so an internet connection is needed on first load.

## Exporting for 3D printing

1. Design your vase with the sliders.
2. Click **Export**.
3. Choose **Format** (STL Binary / STL ASCII / 3MF) and **Resolution** (Coarse / Medium / Fine — higher = smoother mesh, larger file).
4. Export opens the file in your slicer (PrusaSlicer, OrcaSlicer, Cura, etc.). Models are in **millimetres**.

STL Binary is the safe default for FDM printers. 3MF is more compact and carries unit metadata.

## License

**All Rights Reserved.** © 2026 Mark Barretto.

This source code is published for viewing only and may **not** be copied, modified, redistributed, or hosted elsewhere without explicit written permission.

Generated **STL / 3MF design files** produced with this tool are sold separately under their own commercial license terms — see the storefront listing where you obtained them. Personal-use and resale restrictions apply.

## Tech

Vanilla JavaScript + Three.js (ES modules via importmap), single HTML file, CSS custom properties, dark theme. No framework, no bundler.
