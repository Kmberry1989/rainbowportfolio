# Asset Guide

## PNG Layer Requirements

All PNGs should share the same framing and camera perspective.

### bg.png
- Opaque background
- Environment lighting and depth
- No strong foreground shapes

### mid.png
- Primary scene architecture
- Transparent background

### fg.png
- High-intensity neon accents
- Transparent background
- Closest-to-camera detail

### sparks.png
- Particles and energy specks
- Transparent background
- Intended for additive blending

---

## GLB Objects

- Keep poly count moderate.
- Center pivots near object origin.
- Scale around 1.0 units (script rescales to 0.6 by default).

Suggested styles:
- Abstract sculptures
- Tech relics
- Floating artifacts
- Neon geometry

---

## Naming

Scene folders are hardcoded:

```
assets/scenes/scene1/
assets/scenes/scene2/
assets/scenes/scene3/
```

Files expected:

```
bg.png
mid.png
fg.png
sparks.png
```
