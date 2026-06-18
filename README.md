# 🎯 Sprite Sheet Editor

A browser-based tool for defining frame regions on sprite sheets and exporting animation-ready JSON. No server, no build step — a single HTML file.

**Live:** [spritesheet-editor on GitHub Pages](https://bentoobot-netizen.github.io/spritesheet-editor/)

## Features

### Canvas Tools
- **Select (V)** — Click to select frames, shift for multi-select, drag to move
- **Rectangle (R)** — Draw free-form frame regions on the sheet
- **Hand (H)** — Pan the canvas
- **Space+Drag** — Pan (Figma-style)
- **Scroll Wheel** — Zoom in/out (1.04x factor)
- **Marquee Selection** — Drag on empty space to select all frames in rectangle

### Frame Management
- **Resize handles** — 8-point resize on selected frame (Figma-style)
- **Multi-select resize** — Handles on bounding box when 2+ frames selected
- **Snap to Grid (G)** — Cycle through 0/1/2/4/8/16px snap with visual grid overlay
- **Smart Duplicate (Ctrl+D)** — Figma-style repeat offset
- **Arrow Keys** — Move selected frames 1px (Shift: 10px)
- **Drag Reorder** — Drag and drop frames in the sidebar to reorder
- **Frame Naming** — Double-click `#n` in sidebar to name frames (used in export)
- **Align/Distribute** — 8 alignment buttons appear when 2+ frames selected (with custom SVG icons)

### Auto-Detect
- **🔍 Detect** button scans the image for transparent rows/columns and automatically creates frame regions

### Canvas Display
- **Coordinates Bar** — Real-time mouse position (`x, y`) and selection info at bottom
- **Rulers (')** — Toggle horizontal/vertical rulers. Preference saved to localStorage
- **Background Modes** — Cycle between checkerboard / dark / light / custom (click ⬛ button)
- **Onion Skin** — Preview overlay showing previous animation frame at 30% opacity

### Animations
- Define animations with name, timing (ms/fps), and loop toggle
- Play/stop preview in the strip at the bottom
- Color-coded cards for visual grouping

### Export Formats
- **PixiJS** — Standard spritesheet JSON with `frames`, `animations`, and `meta`
- **Phaser 3** — Texture atlas format with `spriteSourceSize`, `sourceSize`, duration-based frames
- **Generic** — Simple `{ frames[], animations[] }` format

Format preference saved to localStorage.

### Undo/Redo
- History stack (max 50), `Ctrl+Z` / `Ctrl+Shift+Z`

### Import
- **PNG Upload** — Drag & drop or click to upload
- **JSON Import** — Load existing spritesheet JSON and recreate frames

### Crop & Reorder
- Visual modal with thumbnails, drag to reorder, export clean sheet + JSON

### Shortcuts
Press `?` or `/` for the full keyboard shortcuts panel.

## Tech

- Single-file vanilla HTML/CSS/JS
- No build step, no server, no dependencies
- Hosts on GitHub Pages or any static host
- Uses Canvas 2D for all rendering

## Development

```bash
# Local dev (any static server)
npx serve .

# Edit
# Just edit index.html — it's a single file

# Deploy to GitHub Pages
git push origin main
```

## License

MIT
