# Three-Body Problem

3D gravitational simulation of the three-body problem. No analytical solution exists — watch chaos emerge.

**[Live Demo](https://2lab-ai.github.io/three-body/)**

## What

Click to spawn up to 3 planets. They interact through Newtonian gravity in 3D space. The second and third bodies automatically receive orbital velocities. Watch as stable orbits break down into chaotic, unpredictable trajectories.

## Controls

| Input | Action |
|-------|--------|
| Click | Spawn planet (max 3) |
| Drag | Orbit camera |
| Scroll | Zoom |
| R | Reset simulation |
| P / Space | Pause/resume |
| T | Toggle trails |
| ← → | Slow down / speed up time |
| C | Center camera on center of mass |
| A | Toggle auto-rotate |

## Physics

- **Integrator**: Velocity Verlet (symplectic, energy-conserving)
- **Gravitational force**: F = G·m₁·m₂/r² with softening
- **Collision**: Elastic bounce with damping
- **Substeps**: 4 per frame for stability
- **Energy monitoring**: bar shows conservation drift

## Features

- Per-body colored trails with speed-based gradient (slow=body color, fast=white)
- Gravity connection lines between bodies (dashed, opacity varies with distance)
- Spawn flash + expanding ring effect
- Glow shells with pulsing animation
- Body-mounted point lights with speed-reactive intensity
- Planet name labels (Alpha, Beta, Gamma)
- Starfield (4000 stars with color variation)
- Reference grid plane
- Time scale control (0.1x to 10x)
- Full touch support

## Tech

Single `index.html` — Three.js from ESM CDN:

```js
import * as THREE from 'https://esm.sh/three@0.172.0'
```

No build step. No dependencies beyond the CDN.

## The Three-Body Problem

In physics, the three-body problem asks for the motion of three masses under mutual gravitational attraction. Unlike the two-body problem (which has a closed-form solution), three-body interactions are chaotic — infinitely sensitive to initial conditions. This simulation lets you see that chaos firsthand.

## Credits

Built by [2lab.ai](https://github.com/2lab-ai)
