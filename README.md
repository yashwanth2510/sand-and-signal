# ABYSSAL ASCII GHOST

An interactive, camera-driven art installation that runs entirely in your browser.
Your webcam becomes the brush — nothing is uploaded, all processing happens locally on your device.

**Live site:** `https://yashwanth2510.github.io/sand-and-signal/`

---

## About

You dissolve into the character stream. Your live form surfaces from the deep as glowing
glyphs rendered in a **green and blue** palette.

- Your shape is drawn from the camera feed as a matrix of ASCII characters.
- Body glyphs and drips randomly mix between electric green and abyssal blue every frame.
- **Movement sets the code on fire:** fast motion spawns `@` bursts and dripping characters.
- Click to send ripples through the depths.
- Pure frame-difference motion detection — no AI models, no dependencies.

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

- Single self-contained HTML file, zero dependencies.
- Canvas 2D rendering at ~60 FPS.
- Mirrored video mapping with cover-fit cropping.
- 96×72 luminance sampler + 64×48 frame-difference motion grid for the ghost.
