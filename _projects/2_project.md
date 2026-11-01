---
layout: page
title: Noncollinear Magnetism and SOC
description: a systematically convergent finite-element framework for fully relativistic pseudopotential DFT
img: assets/img/projects/nc-spin-texture.jpg
importance: 1
category: Computational Method Development
related_publications: true
---

collaborators: Prof. Phani Motamarri

{% cite kodali2024finiteelementmethodsnoncollinearmagnetism %}

Spintronic memory, skyrmionic logic and topological quantum devices all rely on materials where electron spins point in varying directions (noncollinear magnetism) and are coupled to their orbital motion (spin-orbit coupling, SOC). Simulating these effects from first principles requires two-component spinor wavefunctions and spin-dependent Hamiltonians, which makes such calculations considerably more expensive than conventional density functional theory (DFT).

In this project we established a local real-space formulation of noncollinear, spin-orbit-coupled DFT within a finite-element (FE) discretization using fully relativistic optimized norm-conserving Vanderbilt (ONCV) pseudopotentials. Key ingredients include:

- a local reformulation of DFT electrostatics that leads to FE-discretized governing equations for two-component spinors;
- the locally collinear treatment of exchange-correlation, together with regularization strategies that keep GGA functionals well-behaved in regions of vanishing magnetization;
- a unified configurational-force framework, built on a generalized energy functional, that delivers atomic forces and periodic unit-cell stresses for structural relaxation, cell optimization and comparison of competing magnetic configurations.

The methods are implemented in the open-source [DFT-FE](https://github.com/dftfeDevelopers/dftfe) code for both CPU and GPU architectures, and have been validated against established plane-wave codes for energetics, magnetic anisotropy, band structures and spin textures.

<div style="max-width: 760px; margin: 1rem auto 0;">
    <div>
        {% include figure.liquid loading="eager" path="assets/img/projects/nc-spin-texture.jpg" title="Noncollinear magnetization density" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Noncollinear spin texture of a Cr<sub>3</sub> trimer, shown over the underlying finite-element mesh.
</div>
