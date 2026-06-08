# LEGO World Map Builder

Visual editor for creating custom patterns for the **LEGO World Map (#31203)** set — a single-page, dependency-free app that runs in the browser.

**Demo:** https://ppoffal.github.io/lego-map-builder/

![Built with HTML/CSS/JS](https://img.shields.io/badge/stack-vanilla%20HTML%2FJS-orange) ![No build](https://img.shields.io/badge/build-none-green) ![Single file](https://img.shields.io/badge/files-1-blue)

---

## Features

- **Configurable grid** mapped to the physical **16×16 plates** of the set, with highlighted borders and labels (A1, B3, …) to guide assembly
- **Guide image upload** with adjustable opacity — works as a reference underneath the pieces
- **Auto-suggest** — generates the full pattern from the uploaded image, mapping each cell to the nearest LEGO color (perceptual *redmean* distance)
- **3 piece types (1×1 round)**: stud (with knob), flat (tile), and hole, rendered with a 3D effect
- **25 LEGO palette colors** from sets like the World Map and LEGO Art
- **Tools**: paint, erase, bucket fill, eyedropper
- **Piece count** updated in real time, broken down by color + type, both globally and **per plate**
- **Assembly Mode** — toggle that locks editing and opens each plate in a **large modal (≥900px)** with row/column numbering to guide physical assembly
- **Undo (Ctrl+Z)** with a 50-step history — grouping full brush strokes
- **Export PNG** at high resolution, **save/load JSON** pattern file

## How to use

1. Upload a reference photo (`📁 Upload`)
2. Click **✨ Suggest** to auto-generate the pattern
3. Refine cell by cell with the tools
4. When done, enable **🔒 Assembly Mode** and click each plate to see the enlarged view during physical assembly

## Keyboard shortcuts

| Key | Action |
|-----|--------|
| `P` / `B` | Paint |
| `E` | Erase |
| `F` | Fill (bucket) |
| `I` | Eyedropper |
| `1` `2` `3` | Piece type: stud / flat / hole |
| `+` / `-` | Zoom |
| `Ctrl` + `Z` | Undo |
| `Esc` | Close modal (in assembly mode) |
| `←` `→` | Navigate between plates (in modal) |

## Run locally

It's just an HTML file — no server or build step needed:

```bash
git clone https://github.com/ppoffal/lego-map-builder.git
cd lego-map-builder
# Open index.html in your browser
```

Or serve locally:

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Stack

Vanilla **HTML + CSS + JS** in a single `index.html`. Canvas API for rendering. Zero dependencies, zero pipeline.
