---
layout: page
title: HEXA Dense Eigensolver
description: a portable GPU eigensolver for dense symmetric and Hermitian matrices, from one GPU to exascale supercomputers
img: assets/img/projects/hexa-eigensolver.png
importance: 3
category: Computational Method Development
related_publications: false
---

_Ongoing work._

Computing all eigenvalues and eigenvectors of a large dense symmetric or Hermitian matrix is a basic step in electronic-structure calculations, such as the subspace diagonalization of every self-consistent-field iteration in DFT, and in many other fields. Its cost grows as the cube of the matrix size, so for large systems it becomes a bottleneck. On today's GPU supercomputers, the established dense eigensolvers either run on a single GPU or were designed around CPUs, and they leave much of the machines' performance unused when spread over many GPUs.

**HEXA** (Hermitian Eigensolver for eXtreme-scale Accelerators) is a dense eigensolver designed for GPUs from the start. Our aim is a single code base that runs on NVIDIA, AMD and Intel GPUs, in single and double precision, real and complex, and scales from one GPU to thousands without being tuned by hand for each machine. We are evaluating it on Aurora, Frontier and an NVIDIA GH200 system against vendor and distributed libraries, where early results show it outperforming them on all three machines. It is also meant to serve the dense subspace problems in our [exascale DFT work]({{ '/projects/exascale-dft/' | relative_url }}).

<div style="max-width: 720px; margin: 1rem auto 0;">
    <div>
        {% include figure.liquid loading="eager" path="assets/img/projects/hexa-eigensolver.png" title="Dense eigenproblem on many GPUs" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    A dense Hermitian matrix distributed in blocks over a grid of GPUs (each colour one GPU). HEXA computes all of its eigenvalues and eigenvectors.
</div>
