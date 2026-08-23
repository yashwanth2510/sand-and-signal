# SAND & SIGNAL

Two interactive, camera-driven art installations that run entirely in your browser.
Your webcam becomes the brush — nothing is uploaded, all processing happens locally on your device.

**Live site:** `https://<your-username>.github.io/sand-and-signal/`

---

## The Works

### 1. SAND MANDALA — [`mandala.html`](mandala.html)

A sacred pattern draws itself grain by grain, forever.

- **Hand tracking (AI):** MediaPipe Hands recognizes your hand — only your
  fingertips and palm sweep the sand away.
- **5 designs** cycle automatically as each completes:
  Lotus Rings · Star Nest · Temple Geometry · Flower Field · Sunburst.
- Gold markers show where the AI sees your fingers.

| Key | Action |
|-----|--------|
| `N` | next mandala design |
| `C` | clear the sand |
| `F` | fullscreen |
| `H` | hide UI |

### 2. ABYSSAL ASCII GHOST — [`ghost.html`](ghost.html)

You dissolve into the character stream.

- Your live form surfaces from the deep as glowing glyphs in abyssal blues.
- Movement ignites the code: fast motion spawns `@` bursts and dripping characters.
- Click to send ripples through the depths.
- No AI models required — pure frame-difference motion detection.

| Key | Action |
|-----|--------|
| `C` | clear |
| `F` | fullscreen |
| `H` | hide UI |

---

## Running Locally

No build step — each page is a single self-contained HTML file.
Just open `index.html` in any modern browser (Chrome / Edge recommended)
and allow camera access.

> Camera access requires a secure context: `https://`, or `http://localhost`.

## Tech Notes

- **Sand Mandala:** TensorFlow.js + `@tensorflow-models/hand-pose-detection`
  (MediaPipe Hands, lite) loaded from CDN on first run; falls back to simple
  frame-diff erasing while loading or offline.
- **ASCII Ghost:** no dependencies at all.
- Canvas 2D rendering, ~60 FPS, mirrored video mapping with cover-fit cropping.

## Files

```
index.html    landing page linking both works
mandala.html  Sand Mandala (standalone)
ghost.html    Abyssal ASCII Ghost (standalone)
```
