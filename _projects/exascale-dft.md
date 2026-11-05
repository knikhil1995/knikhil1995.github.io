---
layout: page
title: Exascale Relativistic DFT
description: GPU-centric mixed-precision computation and compressed communication for fully relativistic finite-element DFT
img: assets/img/projects/bfp-communication.png
importance: 5
category: Computational Method Development
related_publications: true
---

collaborators: Gourab Panigrahi, Nishant Gupta, Kartick Ramakrishnan, Sundaresan G, Rudra Panch, Sambit Das, Vishwas Rao, Prof. Phani Motamarri

{% cite kodali2026exascalencsoc %}

Modern GPU supercomputers offer far higher throughput for low-precision arithmetic than for double precision, and moving data between devices is often more expensive than computing on it. Eigensolvers in scientific simulations have struggled to exploit either fact without losing accuracy. Building on the robustness of the [R-ChFSI eigensolver]({{ '/projects/rchfsi/' | relative_url }}), this project develops a GPU-centric, exascale-oriented finite-element DFT framework for noncollinear magnetism and spin-orbit coupling that targets both floating-point and data-movement bottlenecks.

The framework combines:

- adaptive higher-order finite-element discretization and a matrix-free Poisson solver;
- GPU-optimized Hamiltonian-multivector products for two-component spinors;
- mixed-precision filtering, with cell-level products in FP32/TF32 while residuals are kept in FP64;
- block floating-point (BFP) compression of the nearest-neighbour halo data exchanged between MPI ranks;
- communication-efficient band parallelization and a distributed blockwise Rayleigh-Ritz procedure.

Together these techniques make systematically convergent, fully relativistic DFT calculations on systems with tens of thousands of electrons practical on leadership-class machines such as Aurora and Frontier. This work has been accepted at SC26.

<div style="max-width: 720px; margin: 1rem auto 0;">
    <div>
        {% include figure.liquid loading="eager" path="assets/img/projects/bfp-communication.png" title="Compressed halo communication" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The finite-element mesh is partitioned across GPUs; the halo data exchanged between neighbouring partitions is compressed to a block floating-point format before communication and decompressed on arrival.
</div>
