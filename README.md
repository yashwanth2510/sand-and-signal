# ABYSSAL ASCII GHOST

An interactive, camera-driven art installation that runs entirely in your browser.
Your webcam becomes the brush — nothing is uploaded, all processing happens locally on your device.

**Live site:** `https://yashwanth2510.github.io/sand-and-signal/`

---

## About

AI maps your **entire body** into a living skeleton of glowing glyphs.

- **Body pose detection (AI):** MediaPipe **BlazePose** (33 full-body keypoints)
  traces your bones — shoulders, arms, hands, spine, hips, legs, feet, and face —
  as a wireframe of ASCII characters.
- Glyphs along each bone randomly mix **electric green** (`#00e676` / `#76ff03`)
  and **abyssal blue** (`#00b0ff` / `#3d5afe`).
- **Movement sets the code on fire:** fast-moving joints spawn dripping `@` embers.
- Falls back to MoveNet if BlazePose fails to load.

| Key | Action |
|-----|--------|
| `C` | clear |
| `F` | fullscreen |
| `H` | hide UI |

---

## Running Locally

No build step — just open `index.html` in any modern browser (Chrome / Edge recommended)
and allow camera access.

> Camera access requires a secure context: `https://`, or `http://localhost`.

## Tech Notes

- Single self-contained HTML file.
- **AI models:** TensorFlow.js + `@tensorflow-models/pose-detection`
  (MediaPipe BlazePose, lite) loaded from CDN on first run.
- Canvas 2D rendering at ~60 FPS.
- Mirrored video mapping with cover-fit cropping.
