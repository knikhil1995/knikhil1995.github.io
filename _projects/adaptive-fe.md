---
layout: page
title: Adaptive-Coordinate Finite Elements
description: moving the finite-element mesh toward the atoms to reduce the cost of real-space DFT
img: assets/img/projects/adaptive-mesh.png
importance: 6
category: Computational Method Development
related_publications: false
---

collaborators: Prof. Phani Motamarri

_Manuscript in preparation._

The size of the discretized Kohn-Sham problem is set by the spatial mesh. Wavefunctions and densities vary sharply near the atomic cores but smoothly in between, so hard pseudopotentials and chemically diverse systems can demand very fine resolution close to the atoms even when the rest of the domain does not need it.

This project develops an adaptive-coordinate extension of our fully relativistic finite-element DFT framework. Instead of adding more elements, an atom-dependent, compactly supported map displaces the nodes of the existing hexahedral mesh toward the atoms, concentrating resolution where it is needed without changing element connectivity. Each element keeps a simple trilinear geometry map while the electronic fields retain their higher-order polynomial approximation.

The Kohn-Sham Hamiltonian, nonlocal pseudopotential projectors, overlap matrix and electrostatics are all evaluated consistently on the moved elements. Because the mesh now depends on the atomic positions, we extended the configurational-force framework to account for the mesh response, so that atomic forces and periodic cell stresses remain consistent with the energy. The approach complements conventional mesh refinement as a route to fewer degrees of freedom for a given accuracy.

<div style="max-width: 720px; margin: 1rem auto 0;">
    <div>
        {% include figure.liquid loading="eager" path="assets/img/projects/adaptive-mesh.png" title="Adaptive-coordinate mesh" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: a conventional locally refined finite-element mesh. Right: the same mesh after the adaptive-coordinate map pulls nodes toward an atom, increasing resolution near the core without adding elements.
</div>
