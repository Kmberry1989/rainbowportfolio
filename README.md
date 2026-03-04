# Neon Universe — Phase 4 (Objects + Deep Space)

An interactive Three.js experience featuring:
- Orbiting memory portals with layered PNG scenes
- A square transparent oscilloscope core with animated techno frame
- Neural portal interactions + camera gravity wells
- Persistent GLB orbiting objects (always visible)
- Deep-space phenomena (nebulas, shooting stars, starfield)
- Bloom postprocessing

## Quick Start

Run a local web server from this project folder:

```bash
python -m http.server 5173
```

Open: http://localhost:5173

(Any static server works.)

## Project Structure

```
neon_universe_project/
├── index.html              # Main app (all logic in one file)
├── README.md               # This file
├── docs/
│   └── ASSET_GUIDE.md      # Asset expectations and naming
└── assets/
    ├── scenes/
    │   ├── scene1/
    │   │   ├── bg.png
    │   │   ├── mid.png
    │   │   ├── fg.png
    │   │   └── sparks.png
    │   ├── scene2/
    │   │   ├── bg.png
    │   │   ├── mid.png
    │   │   ├── fg.png
    │   │   └── sparks.png
    │   └── scene3/
    │       ├── bg.png
    │       ├── mid.png
    │       ├── fg.png
    │       └── sparks.png
    └── objects/
        ├── object1.glb
        ├── object2.glb
        └── object3.glb
```

## Scene Layer Notes (PNG)

Each scene is a layered stack:

- `bg.png` – opaque background plate
- `mid.png` – midground architecture (transparent PNG)
- `fg.png` – foreground neon accents (transparent PNG)
- `sparks.png` – additive particle overlay (transparent PNG)

Recommended size: 2048x1152 (16:9)

## GLB Orbiters

Place `.glb` files into:

```
assets/objects/
```

Default filenames expected:

- object1.glb
- object2.glb
- object3.glb

If files are missing, the app auto-generates emissive fallback shapes.

## Controls

- Move mouse: parallax + gentle camera drift
- Click portal: enter memory scene
- Scroll: zoom (OrbitControls)
- Drag: orbit camera

## Systems Overview

### Core
- Square oscilloscope canvas (1024x1024)
- Transparent center plane
- Animated frame rings + gear-like corners

### Memory Portals
- Orbit around center
- Neural interaction influences energy and motion
- Echo system spreads energy when entering a portal

### Deep Space
- Volumetric-style nebula billboards
- Procedural shooting stars
- High-density starfield

### Post FX
- UnrealBloomPass drives neon glow
- Heartbeat signal modulates bloom intensity

## Troubleshooting

### Black scene / nothing visible
- Make sure you are running a local server (not opening file:// directly).

### Missing PNG or GLB files
- The app will still run, but portals/objects may look empty.
- Verify paths match the folder structure.

### Performance
- Reduce star count or bloom strength in `index.html`.

## License

Project scaffold generated for creative prototyping. Use and modify freely.
