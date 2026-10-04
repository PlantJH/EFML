# FDTD Modeling of Multilayer Reflective Coatings with Nodular Defects

This repository contains a Lumerical FDTD modeling script associated with the manuscript **“Design methods and application of optical reflective films with enhanced laser damage threshold.”**

## Research overview

The study investigates a two-stage coating design approach: standing-wave field modulation using an electric field modulation layer (EFML), followed by particle swarm optimization (PSO) to reduce local electric-field enhancement around nodular defects.

## Repository contents

| File | Description |
| --- | --- |
| `design600.lsf` | Setup script for a multilayer coating with a spherical SiO₂ seed and surrounding coating geometry under 532 nm illumination. |
| `README.md` | Model overview and software requirements. |

The setup script defines coating geometry, a plane-wave source, an FDTD simulation region, and an electric-field monitor. It uses a 19-layer Ta₂O₅/SiO₂ base stack with six additional modulation layers.

## Software and dependencies

The script uses the Ansys Lumerical FDTD scripting language and requires access to Lumerical FDTD. It is not a Python or MATLAB script.

The model uses the refractive-index parameters `n1`, `n2`, and `n3`, and the seed-radius parameter `r` (in micrometers). It references the project material definitions `SIO2`, `Ta2o5-807`, and `SUB`.

## Simulation configuration

- Reference wavelength: 532 nm.
- Illumination: normally incident plane wave propagating along the negative z direction.
- Incident electric-field amplitude: 1 V/m.
- Simulation: two-dimensional FDTD with perfectly matched layer (PML) boundaries.
- Monitoring: an electric-field profile monitor named `E` in the x–z plane.
