# Distortion Wave Playground

Interactive WebGL2 refractive distortion wave playground and live parameter tuner built with zero external dependencies.

## Features

- **Zero-flicker DOM-to-WebGL handoff**: serializes live DOM states via high-DPI SVG `<foreignObject>` preserving root `<html>` attributes (`data-font`, etc.) with an instant canvas cut.
- **Granular wave tuning**: live controls for wave type (`center`, `vertical`, `horizontal`), palettes (`metal`, `ocean`, `sunset`, `green`, `colorful`, `monochromatic`, or custom `#hex`), fixed vs. pointer origin, duration, speed, and all shader optics, mesh, edge-light, and particle parameters.
- **Interactive Bezier curve editor**: live SVG curve preview with presets (including AirDrop steep ease + pull-in/bloom motion).
- **One-click constant export**: copies ready-to-paste `const WAVE_*` declarations directly into `components/distortion-wave.js`.
- **Fullscreen stage test**: previews `trSuccessWave` across the full viewport.

## Run locally

Serve the repository folder over HTTP (required for `<foreignObject>` font inlining and WebGL texture security):

```bash
python -m http.server 8099
```

Then open `http://127.0.0.1:8099/` in a WebGL2-capable browser.

## Deploy on GitHub Pages

1. Publish this repository to GitHub (for example via GitHub Desktop).
2. In **Settings -> Pages**, set Source to **Deploy from a branch** (`main`, `/ (root)`).
3. Open the published GitHub Pages URL directly (`index.html` is the live playground).
